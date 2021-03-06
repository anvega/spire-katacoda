# Refresh application

Click the `Display Port` button if the webapp isn't showing yet (don't change
the port).

Once the page refreshes, you should be looking at a bank transaction log for
"Jacob Marley".

# Delete registration entry

Next, we'll revoke the workload entry for the `customer-service-envoy`
container. We have configured a 30 second TTL for SVIDs, so it will take a
moment for the entry to be revoked, then the application will stop working
(the page refreshes automatically).

`./revoke_envoy`{{execute}}

# Re-create registration entry

If you go back to step 2 and re-run the command to "Create entry for
customer-service-envoy container", then the application will start to work
again once the entry is registered and the workload is reattested.

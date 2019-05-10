# Monitoring and alerting notes

From the operability book:

* Don't use production specific tooling, advocate for test environments to use the same
* Similar to automated checks right? Looking for the expected, not the unknown
* Monitoring informs areas to focus testing for regressions on
* Does the team know what 'normal' operations look like, testing for disruptions to normal based on monitoring
  * Perhaps an exercise on determining what normal looks like?
  * Then implementing the alerting based on that?
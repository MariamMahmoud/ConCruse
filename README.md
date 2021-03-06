# ConCruise
[![CircleCI](https://circleci.com/gh/circleci/circleci-docs.svg?style=shield)](https://circleci.com/gh/MariamMahmoud/ConCruise)

## About this solution
So the bottle neck is in the matching algorithm, in this project I used the brute force way to match, which is okay for small data sets, however in real life applications this is not practical and will cause multiple issues. So here are some suggestions:
- One way is to fetch those  available and in a certain range around me, fetching a smaller array, or even applying more complicated filters in run time those around me, available and withing a certain score from me
        The downside of that is that sometime matching will fail although cruisers are available,
        but that's because there is a huge score gap that would affect the customer satisfaction,
        so it is a business decision what to compromise here
- Another suggestion is to set a threshold, once we get a cruiser that fits this threshold we don't need to continue to loop through all of them.
        we will match this one and compromise the best match for the sake of a faster yet still good match. Again the downside is some mismatching or missing best matching
- I heard about a commonly solution where we would try to find a best match case with a high threshold then if no matches found we would decrease the threshold gradually till a match is found
        This can be a bit faster to find a match and will avoid a no match or mismatch case too

## Tests
Unit tests in this project are not for delivery purposes but just for development to ensure code is behaving as expected at least in happy scenarios

## Usage
- Run `npm run docker-build` to start the container and your apis will be available at `localhost:8080`
- Run `npm run seed` to seed your data
- Run `npm run operations` to use commander

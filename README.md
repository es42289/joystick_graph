# Walker Colt Fast Edit Well Curve Fit Tool Functionality Example

This repo includes a containerized django app which is currently running at http://73.3.239.170:8502/.

The client likes this functionality and wants to move forward with refinement.

## Next steps from my Perspective
1. Need to remove hard coded example data and integrate with Snowflake instance
    - want to be able to toggle between 'fast edit' wells. See get_fast_edit_wells() and get_production_data() from *FAST EDIT.py* streamlit app in Snowflake

2. Need to be able to save the toggled parameters back to snowflake db

3. Need to calculate EUR (estimated ultimate recovery) which is the historic data points and the future curve data points summed to provide total recoverable barrels.
    - Note that the curve fit functionality should and will allow for the calculated curve to go backwards into the hsitoric production section
    - The historic (x-axis date < todays date) volumes calcd from the curve fit should be ignored for calculations

4. Need to add a toggle switch that switches between oil and gas on the graph
    - example only shows oil production volumes
    - db contains gas production data as well
    - user needs to curve fit oil and then switch to curve fit gas
    - need a save button to switch between both
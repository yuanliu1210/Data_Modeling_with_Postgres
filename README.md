{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {
    "editable": true
   },
   "source": [
    "# Schema for Song Play Analysis\n",
    "\n",
    "## Purpose \n",
    "The purpose of creating the Postfres database is to help Sparkify to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to.\n",
    "\n",
    "\n",
    "## Database Schema Design  \n",
    "Using the song and log datasets, I created a star schema optimized for queries on song play analysis. This includes the following tables.\n",
    "\n",
    "### Fact Table\n",
    "1.\t**Songplays** - records in log data associated with song plays i.e. records with page NextSong\n",
    "    •\tsongplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent\n",
    "\n",
    "### Dimension Tables\n",
    "1.\t**Users** - users in the app\n",
    "    •\tuser_id, first_name, last_name, gender, level\n",
    "\n",
    "2.\t**Songs** - songs in music database\n",
    "    •\tsong_id, title, artist_id, year, duration\n",
    "\n",
    "3.\t**Artists** - artists in music database\n",
    "    •\tartist_id, name, location, latitude, longitude\n",
    "\n",
    "4.\t**Time** - timestamps of records in songplays broken down into specific units\n",
    "    •\tstart_time, hour, day, week, month, year, weekday\n",
    "\n",
    "\n",
    "## ETL Pipeline\n",
    "1.\t**Process song_data**\n",
    "In this first part, I performed ETL on the first dataset, song_data, to create the songs and artists dimensional tables.\n",
    "\n",
    "2.\t**Process log_data**\n",
    "In this part, I performed ETL on the second dataset, log_data, to create the time and users dimensional tables, as well as the songplays fact table.\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "editable": true
   },
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.6.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}

{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "960d6c3d",
   "metadata": {},
   "source": [
    "# Optimization of parameters for SMA Strategy\n",
    "\n",
    "## What is this?\n",
    "\n",
    "**Class** for the backtesting of SMA strategies.\n",
    "\n",
    "## Project of Contents\n",
    "\n",
    "- Dataset: Data source from yahoo finance\n",
    "\n",
    "## Main funtion\n",
    "\n",
    "MA_Strategy(ticker_name, MA_Short, MA_Long, start, end)\n",
    " \n",
    "      '''\n",
    "        Input\n",
    "        ----------\n",
    "        ticker_name: str\n",
    "            ticker symbol to be backtested\n",
    "        MA_Short: int\n",
    "            Sliding window in bars (e.g. days) for shorter Simple Moving Average\n",
    "        MA_Long: int\n",
    "            Sliding window in bars (e.g. days) for longer Simple Moving Average\n",
    "        start: str\n",
    "            start date for data import\n",
    "        end: str\n",
    "            end date for data import\n",
    "        ''' \n",
    "\n",
    "      EX.\n",
    "      tester=MA_Strategy(\"2618\",50, 200, \"2019-01-01\", \"2022-06-30\")\n",
    "\n",
    "\n",
    "### Updates SMA parameters and the prepared dataset\n",
    "    tester.set_parameters(SMA_S = 25, SMA_L = 150)\n",
    "    \n",
    "### Backtests the SMA-based trading strategy\n",
    "    tester.test_strategy()\n",
    "    \n",
    "\n",
    "\n",
    "### Plots the performance of the trading strategy and compares to \"buy and hold\"\n",
    "\n",
    "    tester.plot_results()\n",
    " \n",
    " ![png](plot_results.png)\n",
    "  --------------------------\n",
    "### Finds the optimal strategy (global maximum) given the SMA parameter ranges.\n",
    "\n",
    "        '''\n",
    "        Parameters\n",
    "        ----------\n",
    "        SMA_S_range, SMA_L_range: tuple\n",
    "            tuples of the form (start, end, step size)\n",
    "        '''\n",
    "      EX.\n",
    "      tester.optimize_parameters((10, 20, 1), (150, 200, 1))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "4a9562d5",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
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
   "version": "3.8.12"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}

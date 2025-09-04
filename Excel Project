SELECT * FROM CovidDeaths$;
SELECT * FROM CovidVaccinations$;

--EXCEL PROJECT

SELECT SUM(NEW_CASES) AS TOTALCASES,
       SUM(CAST(NEW_DEATHS AS INT)) AS TOTALDEATHS,
	   SUM(CAST(NEW_DEATHS AS INT))/SUM(NEW_CASES)*100 AS DEATHPERCENTAGE
FROM CovidDeaths$
WHERE CONTINENT IS NOT NULL
GROUP BY DATE
ORDER BY 2,3;


Select location, SUM(cast(new_deaths as int)) as TotalDeathCount
From CovidDeaths$
--Where location like '%states%'
Where continent is null 
and location not in ('World', 'European Union', 'International')
Group by location
order by TotalDeathCount desc


Select Location, Population, MAX(total_cases) as HighestInfectionCount,  
       Max((total_cases/population))*100 as PercentPopulationInfected
From CovidDeaths$
--Where location like '%states%'
Group by Location, Population
order by PercentPopulationInfected desc
       

Select Location, Population,date, MAX(total_cases) as HighestInfectionCount,  
       Max((total_cases/population))*100 as PercentPopulationInfected
From CovidDeaths$
--Where location like '%states%'
Group by Location, Population, date
order by PercentPopulationInfected desc

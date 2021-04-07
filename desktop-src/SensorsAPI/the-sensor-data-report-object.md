---
description: L’objet de rapport de données de capteur contient des données de capteur.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Objet de rapport de données de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d43753aa28be5cd20c85b7e65bf4c7516d4c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952367"
---
# <a name="the-sensor-data-report-object"></a><span data-ttu-id="21c2e-103">Objet de rapport de données de capteur</span><span class="sxs-lookup"><span data-stu-id="21c2e-103">The Sensor Data Report Object</span></span>

<span data-ttu-id="21c2e-104">L’objet de rapport de données de capteur contient des données de capteur.</span><span class="sxs-lookup"><span data-stu-id="21c2e-104">The sensor data report object contains sensor data.</span></span>

<span data-ttu-id="21c2e-105">Pour qu’un capteur soit utile, il doit fournir des données significatives.</span><span class="sxs-lookup"><span data-stu-id="21c2e-105">For a sensor to be useful, it must provide meaningful data.</span></span> <span data-ttu-id="21c2e-106">Le volume et la fréquence de génération des données varient d’un capteur à l’autres.</span><span class="sxs-lookup"><span data-stu-id="21c2e-106">The amount and frequency of data generation varies from sensor to sensor.</span></span> <span data-ttu-id="21c2e-107">Par exemple, un capteur qui détecte si une porte est ouverte génère une petite quantité de données **booléennes** , tandis qu’un capteur de mouvement peut générer en continu plusieurs éléments de données.</span><span class="sxs-lookup"><span data-stu-id="21c2e-107">For example, a sensor that detects whether a door is open would generate a small amount of **Boolean** data, while a motion sensor might continuously generate multiple data items.</span></span> <span data-ttu-id="21c2e-108">Pour normaliser le mode de réception des données par votre programme, l’API de capteur utilise l’objet de rapport de données de capteur.</span><span class="sxs-lookup"><span data-stu-id="21c2e-108">To standardize the way your program receives data, the Sensor API uses the sensor data report object.</span></span>

<span data-ttu-id="21c2e-109">Vous pouvez accéder aux informations contenues dans un rapport de données de capteur par le biais de l’interface [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) .</span><span class="sxs-lookup"><span data-stu-id="21c2e-109">You can access the information in a sensor data report through the [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) interface.</span></span> <span data-ttu-id="21c2e-110">Cette interface vous permet de récupérer l’horodatage du rapport de données afin que vous puissiez déterminer si les informations contenues dans le rapport sont utiles.</span><span class="sxs-lookup"><span data-stu-id="21c2e-110">This interface lets you retrieve the data report's time stamp so that you can determine whether the information in the report is useful.</span></span> <span data-ttu-id="21c2e-111">Vous pouvez récupérer les données de deux manières : en tant que valeur de champ de données individuel ou en tant qu’ensemble de valeurs.</span><span class="sxs-lookup"><span data-stu-id="21c2e-111">You can retrieve the data itself in two ways: as an individual data field value or as a set of values.</span></span> <span data-ttu-id="21c2e-112">Pour récupérer des données en tant que valeur individuelle, appelez la méthode [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) .</span><span class="sxs-lookup"><span data-stu-id="21c2e-112">To retrieve data as an individual value, call the [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) method.</span></span> <span data-ttu-id="21c2e-113">Pour récupérer plusieurs valeurs, appelez la méthode [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) .</span><span class="sxs-lookup"><span data-stu-id="21c2e-113">To retrieve multiple values, call the [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) method.</span></span>

<span data-ttu-id="21c2e-114">Vous spécifiez le type de données ou les champs de données que vous souhaitez extraire du rapport à l’aide d’une constante **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="21c2e-114">You specify the type of data, or data fields, that you want to retrieve from the report by using a **PROPERTYKEY** constant.</span></span> <span data-ttu-id="21c2e-115">Les clés de propriété pour les champs de données des types de capteurs communs sont définies dans sensors. h.</span><span class="sxs-lookup"><span data-stu-id="21c2e-115">Property keys for data fields of common sensor types are defined in Sensors.h.</span></span>

 

 

---
description: L’objet de rapport de données de capteur contient des données de capteur.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Objet de rapport de données de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca1a8e5f61b23753437bd8b1cf4c2a176515b7042b21e84c4d2f431debc8fe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992599"
---
# <a name="the-sensor-data-report-object"></a>Objet de rapport de données de capteur

L’objet de rapport de données de capteur contient des données de capteur.

Pour qu’un capteur soit utile, il doit fournir des données significatives. Le volume et la fréquence de génération des données varient d’un capteur à l’autres. Par exemple, un capteur qui détecte si une porte est ouverte génère une petite quantité de données **booléennes** , tandis qu’un capteur de mouvement peut générer en continu plusieurs éléments de données. Pour normaliser le mode de réception des données par votre programme, l’API de capteur utilise l’objet de rapport de données de capteur.

Vous pouvez accéder aux informations contenues dans un rapport de données de capteur par le biais de l’interface [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) . Cette interface vous permet de récupérer l’horodatage du rapport de données afin que vous puissiez déterminer si les informations contenues dans le rapport sont utiles. Vous pouvez récupérer les données de deux manières : en tant que valeur de champ de données individuel ou en tant qu’ensemble de valeurs. Pour récupérer des données en tant que valeur individuelle, appelez la méthode [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) . Pour récupérer plusieurs valeurs, appelez la méthode [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) .

Vous spécifiez le type de données ou les champs de données que vous souhaitez extraire du rapport à l’aide d’une constante **PROPERTYKEY** . Les clés de propriété pour les champs de données des types de capteurs communs sont définies dans sensors. h.

 

 

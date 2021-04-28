---
description: Bibliothèque de Registre hors connexion
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Bibliothèque de Registre hors connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089247"
---
# <a name="offline-registry-library"></a>Bibliothèque de Registre hors connexion

## <a name="purpose"></a>Objectif

La bibliothèque de Registre hors connexion (Offreg.dll) est utilisée pour modifier une ruche de registre en dehors du Registre système actif. Cette bibliothèque est destinée aux scénarios de mise à jour du Registre tels que la maintenance d’une image du système d’exploitation. La bibliothèque prend en charge les formats Hive de Registre à partir de Windows Vista.

## <a name="developer-audience"></a>Développeurs concernés

Cette technologie est destinée aux fabricants OEM (Original Equipment Manufacturers), aux éditeurs de logiciels anti-programme malveillant et à d’autres développeurs d’applications qui doivent être en mesure d’analyser les fichiers ruche du registre sans les charger dans le Registre actif.

## <a name="run-time-requirements"></a>Conditions d’exécution

La bibliothèque de Registre hors connexion est fournie sous la forme d’une bibliothèque de liens dynamiques (DLL) redistribuable binaire. Cette bibliothèque s’exécute sur les versions suivantes de Windows :

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
Windows Server 2008  
Windows Vista  
</dl>

Les applications doivent être liées à Offreg.dll à l’aide de la liaison dynamique.

Offreg.dll est fourni dans le kit de pilotes Windows (WDK) pour Windows 10 et les versions antérieures du système d’exploitation Windows.

Pour plus d’informations sur l’obtention du kit WDK, consultez [Comment obtenir le kit WDK et le WLK](/windows-hardware/drivers/download-the-wdk) ou visitez le site Web des [abonnements MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .

## <a name="in-this-section"></a>Contenu de cette section

-   [**À propos de la bibliothèque de Registre hors connexion**](about-the-offline-registry-library.md)
-   [**Fonctions de la bibliothèque de Registre hors connexion**](offline-registry-library-functions.md)

 

 

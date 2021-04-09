---
description: Les classes de gestion de service WMI sont utilisées pour gérer le service WMI lui-même, et non le système informatique ou le réseau d’entreprise. La gestion de WMI englobe la configuration du service WMI et la gestion des opérations WMI.
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: Classes de gestion des services WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110214"
---
# <a name="wmi-service-management-classes"></a>Classes de gestion des services WMI

Les classes de gestion de service WMI sont utilisées pour gérer le service WMI lui-même, et non le système informatique ou le réseau d’entreprise. La gestion de WMI englobe la configuration du service WMI et la gestion des opérations WMI.

La catégorie gestion des services WMI comprend les sous-catégories de classes suivantes :

-   [Classes de configuration WMI](#wmi-configuration-classes)
-   [Classes de gestion WMI](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a>Classes de configuration WMI

La classe de configuration WMI dérive les méthodes qui configurent le service WMI.

Voici un tableau des classes de configuration WMI.



| Classe                                                             | Description                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_MethodParameterClass Win32**](win32-methodparameterclass.md) | Abstraite, classe de base qui implémente les paramètres de méthode dérivés de cette classe. |



 

## <a name="wmi-management-classes"></a>Classes de gestion WMI

Les classes de gestion WMI représentent les paramètres opérationnels du service WMI.

Voici un tableau des classes de gestion WMI.



| Classe                                                       | Description                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_WMISetting Win32**](win32-wmisetting.md)               | Contient les paramètres opérationnels du service WMI.                                      |
| [**\_WMIElementSetting Win32**](win32-wmielementsetting.md) | Association entre un service s’exécutant dans le système Windows et les paramètres WMI qu’il peut utiliser. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes Win32](./win32-provider.md)
</dt> </dl>

 

 

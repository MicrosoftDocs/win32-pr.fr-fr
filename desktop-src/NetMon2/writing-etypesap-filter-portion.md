---
description: La partie ETYPE/SAP du filtre de capture notifie au pilote Moniteur réseau d’accepter des frames qui ont une combinaison spécifique de ETYPE et de points d’accès de service (SAP).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Écriture de la portion de filtre ETYPE/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da18b8e2d7d5fc081ea941070644379e6e988a5c697b7ee09ee76a8fdd0c083e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036789"
---
# <a name="writing-etypesap-filter-portion"></a>Écriture de la portion de filtre ETYPE/SAP

La partie ETYPE/SAP du filtre de capture notifie au pilote Moniteur réseau d’accepter des frames qui ont une combinaison spécifique de ETYPE et de [*points d’accès de service*](s.md) (SAP). Les types ETYPE et SAP sont les deux façons dont les protocoles de bas niveau tels que Ethernet, LLC et Snap indiquent le protocole qui les suit. En particulier :

-   Ethernet spécifie un ETYPE
-   LLC spécifie un SAP
-   Le magnétisme spécifie un ETYPE

## <a name="etypesap-capture-filter-flags"></a>Indicateurs de filtre de capture ETYPE/SAP

Utilisez les informations suivantes pour définir les indicateurs dans le membre **FilterFlags** de la structure [**capturefilter**](capturefilter.md) .



| Indicateur                                         | Signification                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_les indicateurs capturefilter \_ incluent \_ tous les \_ SAP   | Transmet toutes les valeurs SAP et notifie au pilote que toutes les valeurs SAP sont valides. En cas de combinaison avec toutes les valeurs du membre **lpSapTable** , cet indicateur informe le pilote que toutes les valeurs SAP, à l’exception de celles du **lpSapTable** , sont valides.<br/>           |
| \_les indicateurs capturefilter \_ incluent \_ tous les \_ ETYPE | Passe toutes les valeurs ETYPE et notifie au pilote que toutes les valeurs ETYPE sont valides. En cas de combinaison avec toutes les valeurs du membre **lpEtypeTable** , cet indicateur informe le pilote que toutes les valeurs ETYPE, à l’exception de celles du **lpEtypeTable** , sont valides.<br/> |
| \_indicateurs capturefilter \_ locaux \_ uniquement           | La définition de cet indicateur ne définit pas une carte réseau en mode P. Vous verrez uniquement le trafic local (tous les frames sur l’ordinateur local).                                                                                                                                          |
| les \_ indicateurs capturefilter \_ conservent \_ RAW             | Conserve les trames de SMT et Token Ring MAC.                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a>filtre de Capture Etype/SAP Paramètres

Utilisez les informations suivantes pour définir les membres **lpSapTable** et **lpEtypeTable** de la structure [**capturefilter**](capturefilter.md) .



| Paramètre          | Signification                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lpSapTable**   | Répertorie les valeurs SAP que le pilote doit passer. Cette liste indique au pilote Moniteur réseau de valider les frames qui contiennent une correspondance. Si \_ les indicateurs capturefilter \_ incluent \_ tous les \_ SAP sont définis, cela devient une liste d’exceptions (si elle est trouvée, ne réussit pas).           |
| **lpEtypeTable** | Répertorie les valeurs ETYPE que vous souhaitez que le pilote de Moniteur réseau passe. Cette liste indique uniquement au pilote de valider toute trame qui contient une correspondance. Si \_ les indicateurs capturefilter \_ incluent \_ tous les \_ ETYPE sont définis, cela devient une liste d’exceptions (si elle est trouvée, ne passe pas). |



 

 

 





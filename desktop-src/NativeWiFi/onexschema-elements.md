---
description: Un profil 802.1 X contient les éléments de schéma suivants.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Éléments de schéma OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119397"
---
# <a name="onex-schema-elements"></a>Éléments de schéma OneX

Un profil 802.1 X contient les éléments de schéma suivants. Tous les éléments de schéma OneX s’appliquent aux profils filaires et sans fil. La plupart des éléments nommés se trouvent dans l’espace de noms `https://www.microsoft.com/networking/OneX/v1` , à l’exception de [**EAPConfig (Onex)**](onexschema-eapconfig-onex-element.md) qui se trouve dans l’espace de noms `https://www.microsoft.com/provisioning/EapHostConfig` .

La liste suivante présente les éléments définis dans l’ordre dans lequel les éléments apparaissent dans un profil. L’ordre des éléments est appliqué. Tous les éléments ne se trouvent pas dans chaque profil, car certains éléments sont facultatifs.

Cette liste n’affiche pas tous les éléments possibles qui peuvent apparaître dans un profil, car des éléments peuvent être ajoutés dans **XS : n’importe quel** point d’insertion.

-   [**802.1x**](onexschema-onex-element.md)
    -   [**cacheUserData (OneX)**](onexschema-cacheuserdata-onex-element.md)
    -   [**heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
    -   [**authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
    -   [**startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
    -   [**maxStart (OneX)**](onexschema-maxstart-onex-element.md)
    -   [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
    -   [**supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
    -   [**authMode (OneX)**](onexschema-authmode-onex-element.md)
    -   [**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
        -   [**type (singleSignOn)**](onexschema-type-singlesignon-element.md)
        -   [**maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md)
        -   [**userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)

 

 




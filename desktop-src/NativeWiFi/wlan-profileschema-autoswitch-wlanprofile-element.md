---
description: Détermine le comportement d’itinérance d’un réseau connecté automatiquement lorsqu’un réseau plus préféré est à portée.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: AutoSwitch (WLANProfile) (élément)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863346"
---
# <a name="autoswitch-wlanprofile-element"></a>AutoSwitch (WLANProfile) (élément)

L’élément AutoSwitch (WLANProfile) détermine le comportement d’itinérance d’un réseau connecté automatiquement lorsqu’un réseau plus préféré est à portée. . Cet élément est facultatif.

Si AutoSwitch a la valeur « true » et que [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) est défini sur « auto », une connexion à un réseau plus favori doit être tentée chaque fois qu’un réseau préféré est mis en plage. Un réseau plus favori est un réseau qui est classé plus haut dans la liste des réseaux sans fil préférés. Cette tentative de connexion se produit lorsqu’elle est connectée à un autre réseau.

Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) a la valeur « auto », cette valeur peut être « true » ou « false ».

Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) est défini sur « Manual », cette valeur doit être définie sur « false ». Cet élément n’a aucun effet sur un réseau connecté manuellement.

Une valeur de commutation automatique définie sur « true » entraîne une fréquence plus élevée d’analyse périodique des nouveaux réseaux. Cela peut entraîner une pollution accrue de la fréquence radio par rapport à ces analyses périodiques et une consommation énergétique accrue utilisée par la carte réseau sans fil.

**Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé :** Les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil. Ces modifications sont conçues pour réduire la pollution de la fréquence radio, la consommation d’énergie et l’interruption du trafic en temps réel sur les réseaux sans fil. Le paramètre par défaut pour **AutoSwitch** lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé. La valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé. Le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista. Il est recommandé que la valeur de l’élément **AutoSwitch** utilisé par une application dans un profil de réseau local sans fil soit définie sur « false » pour réduire la fréquence de l’analyse périodique des nouveaux réseaux, à moins qu’il soit absolument nécessaire pour une application de définir cette valeur sur « true ».

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

L’élément **AutoSwitch** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **AutoSwitch** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 





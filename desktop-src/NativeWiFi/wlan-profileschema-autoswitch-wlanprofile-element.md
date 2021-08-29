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
ms.openlocfilehash: a656667a8c32d4b21793cfc605654f1c80c31ce1d69fd274a7be81078f6cc2c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799929"
---
# <a name="autoswitch-wlanprofile-element"></a>AutoSwitch (WLANProfile) (élément)

L’élément AutoSwitch (WLANProfile) détermine le comportement d’itinérance d’un réseau connecté automatiquement lorsqu’un réseau plus préféré est à portée. . Cet élément est facultatif.

Si AutoSwitch a la valeur « true » et que [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) est défini sur « auto », une connexion à un réseau plus favori doit être tentée chaque fois qu’un réseau préféré est mis en plage. Un réseau plus favori est un réseau qui est classé plus haut dans la liste des réseaux sans fil préférés. Cette tentative de connexion se produit lorsqu’elle est connectée à un autre réseau.

Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) a la valeur « auto », cette valeur peut être « true » ou « false ».

Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) est défini sur « Manual », cette valeur doit être définie sur « false ». Cet élément n’a aucun effet sur un réseau connecté manuellement.

Une valeur de commutation automatique définie sur « true » entraîne une fréquence plus élevée d’analyse périodique des nouveaux réseaux. Cela peut entraîner une pollution accrue de la fréquence radio par rapport à ces analyses périodiques et une consommation énergétique accrue utilisée par la carte réseau sans fil.

**Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé :** les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil. Ces modifications sont conçues pour réduire la pollution de la fréquence radio, la consommation d’énergie et l’interruption du trafic en temps réel sur les réseaux sans fil. Le paramètre par défaut pour **AutoSwitch** lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé. la valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le Service de réseau local sans fil installé. le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista. Il est recommandé que la valeur de l’élément **AutoSwitch** utilisé par une application dans un profil de réseau local sans fil soit définie sur « false » pour réduire la fréquence de l’analyse périodique des nouveaux réseaux, à moins qu’il soit absolument nécessaire pour une application de définir cette valeur sur « true ».

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 





---
description: Obtient la version du moteur de traitement WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866230"
---
# <a name="getclientversion-function"></a>getClientVersion fonction)

Obtient la version du moteur de traitement WPAD.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Chaîne délimitée par des points-virgules contenant des adresses IP.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Liste d’adresses IP séparées par des points-virgules triées ou une chaîne vide si le tri de la liste d’adresses IP est impossible.

## <a name="remarks"></a>Notes

Actuellement, cette fonction retourne la version 1,0.

Microsoft a ajouté cette fonction pour permettre aux administrateurs informatiques de mettre à jour leurs scripts WPAD afin d’utiliser différentes versions du moteur de traitement WPAD sans causer de ruptures au déploiement existant. Par exemple, si Microsoft a ajouté une fonction à la version 2,0 du moteur WPAD, les administrateurs peuvent vérifier la version avant de tenter d’appeler cette fonction. Cela permet à leur script de fonctionner avec le client exécutant les versions 1,0 et 2,0 du moteur WPAD.

## <a name="examples"></a>Exemples

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Définitions d’API d’assistance du proxy compatibles IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensions IPv6 du format de fichier de configuration automatique du navigateur](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




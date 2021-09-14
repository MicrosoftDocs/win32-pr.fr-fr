---
description: Spécifie si les machines utilisent le service de configuration automatique intégré pour gérer les connexions aux réseaux câblés qui requièrent l’authentification de couche 2 (par exemple, 802.1 X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: enableAutoConfig (globalFlags), élément (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011590"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a>enableAutoConfig (globalFlags), élément (LAN_policy)

L’élément **enableAutoConfig** (globalFlags) spécifie si les machines utilisent le service de configuration automatique intégré pour gérer les connexions aux réseaux câblés qui requièrent l’authentification de couche 2 (par exemple, 802.1 x).

Lorsque **enableAutoConfig** a la valeur false, les ordinateurs ne doivent pas utiliser le service de configuration automatique intégré pour gérer les connexions qui requièrent l’authentification de couche 2. Au lieu de cela, le réseau spécifié dans l’élément [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) est le seul réseau disponible pour la connexion. Le service de configuration automatique répond uniquement aux demandes d’activation du service.

Lorsque **enableAutoConfig** a la valeur true, les machines peuvent utiliser le service de configuration automatique intégré pour se connecter aux réseaux câblés qui requièrent l’authentification de couche 2.

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

L’élément **enableAutoConfig** est défini par l’élément [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**globalFlags (LANPolicy)**](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 





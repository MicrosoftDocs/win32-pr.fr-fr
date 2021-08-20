---
description: Spécifie s’il s’agit du profil par défaut pour l’appareil.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Élément IsDefault (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: 7dada4789b0a1c1f11676359972eeff074928ca064c04679e35fb7e83132ef53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065903"
---
# <a name="isdefault-mbnprofile-element"></a>Élément IsDefault (MBNProfile)

L’élément **IsDefault (MBNProfile)** spécifie s’il s’agit du profil par défaut pour l’appareil.

Il s’agit d’un élément facultatif et, s’il n’est pas spécifié, le profil n’est pas défini comme profil par défaut.

Le profil par défaut est utilisé par le service haut débit mobile pour les besoins suivants :

-   Le service haut débit mobile utilise les paramètres de connexion du profil par défaut lors de l’exécution de connexions réseau automatiques. Ces paramètres incluent le nom du point d’accès, le nom d’utilisateur, le mot de passe, etc.
-   La stratégie de connexion automatique pour un appareil haut débit mobile est tirée de son profil par défaut.
-   L’interface utilisateur de la connexion réseau du système d’exploitation utilise également les données de connexion du profil par défaut pour les opérations de connexion.

Les fournisseurs de services mobiles peuvent fournir les détails de connexion dans un profil et configurer ce profil comme profil par défaut. Le service haut débit mobile utilise ces paramètres de connexion sans inviter l’utilisateur à entrer des détails.

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

L’élément **IsDefault** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 





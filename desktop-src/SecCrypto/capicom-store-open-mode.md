---
description: Utilisé avec la méthode Store. Open pour indiquer le mode d’ouverture d’un magasin de certificats.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Énumération CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ebd46b751f4a098361618f3b6e992e4333425f501bf6afdedfca047e921ad7ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772056"
---
# <a name="capicom_store_open_mode-enumeration"></a>\_ \_ Énumération du mode d’ouverture d’un magasin CAPICOM \_

Le \_ type d’énumération du mode d’ouverture du magasin CAPICOM \_ \_ est utilisé avec la méthode [**Store. Open**](store-open.md) pour indiquer comment un magasin de certificats doit être ouvert.

## <a name="members"></a>Membres



| Membre                                      | Description                                                                                                                                                              | Valeur |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **le magasin CAPICOM \_ est \_ ouvert \_ en lecture \_ seule**        | Ouvrez le magasin en lecture seule.<br/>                                                                                                                             | 0     |
| **ouverture de la \_ \_ \_ lecture écriture du \_ magasin CAPICOM**       | Ouvrez le magasin en mode lecture/écriture.<br/>                                                                                                                            | 1     |
| **\_ \_ \_ maximum \_ autorisé pour le magasin CAPICOM**  | Ouvre le magasin en mode lecture/écriture si l’utilisateur dispose d’autorisations de lecture/écriture. Si l’utilisateur n’a pas d’autorisations de lecture/écriture, ouvrez le magasin en mode lecture seule.<br/> | 2     |
| **le magasin CAPICOM \_ est \_ ouvert \_ \_ uniquement**    | Ouvrir les magasins existants uniquement ; ne créez pas de nouveau magasin. Introduit par CAPICOM 2,0.<br/>                                                                              | 128   |
| **l’ouverture du \_ magasin \_ CAPICOM \_ inclut \_ Archived** | Incluez les certificats archivés lors de l’utilisation du magasin. Introduit par CAPICOM 2,0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Remarques

Lors de l’utilisation de l' \_ \_ énumération du mode d’ouverture d’un magasin CAPICOM \_ , vous pouvez utiliser un seul des paramètres suivants.

-   le magasin CAPICOM \_ est \_ ouvert \_ en lecture \_ seule
-   ouverture de la \_ \_ \_ lecture écriture du \_ magasin CAPICOM
-   \_ \_ \_ maximum \_ autorisé pour le magasin CAPICOM

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> </dl>

 

 





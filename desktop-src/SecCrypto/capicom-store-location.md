---
description: Indique l’emplacement d’un magasin de certificats.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Énumération CAPICOM_STORE_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 15aa93b70840e13901f88c40c715024ec33a835be14b7453da99aecae079b487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879009"
---
# <a name="capicom_store_location-enumeration"></a>\_Énumération de l’emplacement du magasin CAPICOM \_

Le type d’énumération de l' **\_ \_ emplacement du magasin CAPICOM** indique l’emplacement d’un [*magasin de certificats*](../secgloss/c-gly.md).

## <a name="members"></a>Membres



| Membre                                      | Description                                                                                                                                                                                                                                                                      | Valeur |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_magasin mémoire CAPICOM \_**                  | Le magasin est un magasin de mémoire. Les modifications apportées au contenu du magasin ne sont pas conservées.<br/>                                                                                                                                                                              | 0     |
| **base de l' \_ ordinateur local CAPICOM \_ \_**          | Le magasin est un magasin de l’ordinateur local. Les magasins d’ordinateurs locaux peuvent être des magasins de lecture/écriture uniquement si l’utilisateur dispose d’autorisations de lecture/écriture. Si l’utilisateur dispose d’autorisations de lecture/écriture et si le magasin est ouvert en lecture/écriture, les modifications apportées au contenu du magasin sont conservées.<br/> | 1     |
| **magasin de l' \_ utilisateur actuel CAPICOM \_ \_**           | Le magasin est un magasin de l’utilisateur actuel. Un magasin de l’utilisateur actuel peut être un magasin en lecture/écriture. Si c’est le cas, les modifications apportées au contenu du magasin sont conservées.<br/>                                                                                                                      | 2     |
| **magasin d’utilisateurs de CAPICOM \_ active \_ Directory \_ \_** | Le magasin est un magasin de Active Directory. Les magasins de Active Directory ne peuvent être ouverts qu’en mode lecture seule. Impossible d’ajouter ou de supprimer des certificats dans des magasins de Active Directory.<br/>                                                                                        | 3     |
| **\_magasin d’utilisateurs de \_ carte à puce \_ CAPICOM \_**       | Les magasins prennent en charge les magasins de certificats basés sur une carte à puce. Le magasin est le groupe de cartes à puce actuelles. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Remarques

Le type d’énumération de l' **\_ \_ emplacement du magasin CAPICOM** est utilisé par les méthodes suivantes :

-   [**PrivateKey. Open**](privatekey-open.md)
-   [**Store. Open**](store-open.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 

---
description: L’énumération de l’utilisation de la \_ clé CAPICOM \_ définit la manière dont une clé peut être utilisée. Introduit dans CAPICOM 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Énumération CAPICOM_KEY_USAGE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121090"
---
# <a name="capicom_key_usage-enumeration"></a>\_ \_ Énumération de l’utilisation de la clé CAPICOM

L’énumération de l' **\_ \_ utilisation de la clé CAPICOM** définit la manière dont une clé peut être utilisée. Introduit dans CAPICOM 2,0.

## <a name="members"></a>Membres



| Membre                                      | Description                                                                                                                      | Valeur      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **utilisation de la \_ \_ clé de signature numérique \_ CAPICOM \_** | La clé peut être utilisée pour créer une signature numérique.<br/>                                                                    | 0x00000080 |
| **utilisation de la \_ clé de non- \_ RÉPUDIation CAPICOM \_ \_**   | La clé peut être utilisée pour la non- [*répudiation*](../secgloss/n-gly.md).<br/> | 0x00000040 |
| **utilisation de la \_ \_ clé de chiffrement de la clé CAPICOM \_ \_**  | La clé peut être utilisée pour chiffrer une clé.<br/>                                                                                 | 0x00000020 |
| **utilisation de la \_ \_ clé de chiffrement des données CAPICOM \_ \_** | La clé peut être utilisée pour chiffrer les données.<br/>                                                                                  | 0x00000010 |
| **utilisation de la \_ \_ clé de \_ \_ l’accord de clé CAPICOM**     | La clé peut être utilisée pour l’accord de clé.<br/>                                                                                | 0x00000008 |
| **utilisation de la \_ \_ clé de \_ signature du certificat \_ de clé \_ CAPICOM**    | La clé peut être utilisée pour la signature de certificat de clé. Cette valeur est équivalente à \_ l’utilisation de la \_ clé de signature de la liste de révocation de certificats en mode hors connexion \_ \_ \_ .<br/> | 0x00000004 |
| **\_ \_ utilisation de la clé de signature de la liste de révocation de certificats hors connexion CAPICOM \_ \_ \_** | La clé peut être utilisée pour la signature de certificat de clé. Cette valeur est équivalente à l’utilisation de la \_ clé de signature du certificat de clé CAPICOM \_ \_ \_ \_ .<br/>    | 0x00000002 |
| **\_utilisation de la \_ clé de signature de la liste de révocation de certificats CAPICOM \_ \_**          | La clé peut être utilisée pour la signature.<br/>                                                                                      | 0x00000002 |
| **utilisation de la \_ clé d’ENchiffrement CAPICOM \_ uniquement \_ \_**     | La clé peut uniquement être utilisée pour chiffrer.<br/>                                                                                  | 0x00000001 |
| **l’utilisation de la clé pour le \_ déchiffrement de CAPICOM \_ uniquement \_ \_**     | La clé ne peut être utilisée que pour le déchiffrement.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 

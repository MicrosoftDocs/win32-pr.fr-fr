---
description: Définit les conditions pour lesquelles une chaîne de certificats doit être vérifiée.
ms.assetid: 87df623c-5661-4325-8dd6-393ce2e44066
title: Énumération CAPICOM_CHECK_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CHECK_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 47b6168fb87ebbb65b07eadfe9adaf488934e252
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530395"
---
# <a name="capicom_check_flag-enumeration"></a>\_Énumération de l’indicateur de vérification CAPICOM \_

Le type d’énumération de l' **\_ \_ indicateur de vérification CAPICOM** définit les conditions pour lesquelles une chaîne de certificats doit être vérifiée.

## <a name="members"></a>Membres



| Membre                                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Valeur      |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **vérification de CAPICOM \_ \_ aucun**                        | Aucune vérification de validité n’est effectuée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000000 |
| **CAPICOM vérifier la \_ \_ racine approuvée \_**               | Recherche une racine approuvée de la chaîne de certificats.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000001 |
| **vérification de la \_ validité de la durée du contrôle CAPICOM \_ \_**              | Vérifie la validité de tous les certificats de la chaîne.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 0x00000002 |
| **vérification de la \_ validité de la \_ signature de CAPICOM \_**         | Recherche des signatures valides sur tous les certificats de la chaîne.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 0x00000004 |
| **\_vérifier l’état de \_ \_ révocation en \_ ligne de CAPICOM**  | Vérifie l’état de révocation de tous les certificats de la chaîne à l’aide des listes de révocation de certificats (CRL) disponibles en ligne. Les listes de révocation de certificats sont téléchargées à l’aide de l’extension de point de distribution CRL dans le certificat. <br/> Si la liste de révocation de certificats a été téléchargée et n’a pas expiré, CAPICOM l’utilise et ne passe pas en ligne. Si une liste de révocation de certificats n’a pas été téléchargée ou est obsolète, CAPICOM se met en ligne pour tenter de télécharger la liste de révocation de certificats.<br/> Cet indicateur est ignoré si la \_ case à cocher Vérifier l' \_ État de \_ révocation hors connexion \_ est également spécifiée.<br/> | 0x00000008 |
| **\_vérifier l’état de \_ \_ révocation hors \_ connexion dans CAPICOM** | Vérifie l’état de révocation de tous les certificats de la chaîne en utilisant uniquement les listes de révocation de certificats hors connexion. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              | 0x00000010 |
| **vérification de la \_ \_ chaîne complète de CAPICOM \_**             | Vérifie la chaîne complète. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | 0x00000020 |
| **\_vérifier les contraintes de \_ nom dans CAPICOM \_**           | Vérifie les contraintes de nom. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | 0x00000040 |
| **CAPICOM- \_ vérifier les \_ contraintes de base \_**          | Vérifie les contraintes de base. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | 0x00000080 |
| **vérification de la \_ \_ période de validité imbriquée pour \_ CAPICOM \_**    | Vérifie la validité imbriquée. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | 0x00000100 |
| **CAPICOM- \_ vérifier \_ en ligne \_ tout**                 | Vérifie toutes les conditions, à l’exception de la \_ case à cocher Vérifier l' \_ \_ État de révocation hors connexion \_ . Les vérifications de révocation sont effectuées sur tous les certificats de la chaîne, à l’exception du certificat racine. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                               | 0x000001EF |
| **\_vérification CAPICOM \_ tout en mode hors connexion \_**                | Vérifie toutes les conditions, à l’exception de l' \_ \_ État de révocation en ligne de CAPICOM \_ \_ . Les vérifications de révocation sont effectuées sur tous les certificats de la chaîne, à l’exception du certificat racine. Introduit dans CAPICOM 2,0.<br/>                                                                                                                                                                                                                                                                                                                                | 0x000001F7 |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 





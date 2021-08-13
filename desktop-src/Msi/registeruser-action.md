---
description: L’action RegisterUser enregistre les informations utilisateur avec le programme d’installation pour identifier l’utilisateur d’un produit.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Action RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89d43d18839e806939b7a084d37840b9895fdc81efb79fc03867eebe4c5c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626714"
---
# <a name="registeruser-action"></a>Action RegisterUser

L’action RegisterUser enregistre les informations utilisateur avec le programme d’installation pour identifier l’utilisateur d’un produit.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action   |
|-------|------------------------------|
| \[1\] | Informations sur l’utilisateur inscrit. |



 

## <a name="remarks"></a>Remarques

L’action RegisterUser n’est pas effectuée au cours d’une installation d’administration. Si l’identificateur de produit entré par l’utilisateur n’a pas été validé par l' [Action ValidateProductID](validateproductid-action.md), la propriété [**ProductID**](productid.md) n’est pas définie et cette action n’a aucun effet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**NOM d’utilisateur**](username.md)
</dt> <dt>

[**PRENNENT**](companyname.md)
</dt> <dt>

[**Réf**](productid.md)
</dt> </dl>

 

 




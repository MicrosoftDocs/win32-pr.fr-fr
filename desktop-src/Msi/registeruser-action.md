---
description: L’action RegisterUser enregistre les informations utilisateur avec le programme d’installation pour identifier l’utilisateur d’un produit.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Action RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009680"
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

 

 




---
description: Vous ne pouvez pas créer d’instances des classes modifiées dans l’espace de noms localisé. Les classes modifiées dans l’espace de noms localisé sont traitées comme si elles étaient abstraites, bien qu’elles ne contiennent pas de qualificateur abstrait.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Considérations relatives aux classes modifiées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cd38bc6134c4fd3596cc36e8a7638eaa1fd6ed264c90302d921a391982e5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320238"
---
# <a name="amended-class-considerations"></a>Considérations relatives aux classes modifiées

Vous ne pouvez pas créer d’instances des classes modifiées dans l’espace de noms localisé. Les classes modifiées dans l’espace de noms localisé sont traitées comme si elles étaient abstraites, bien qu’elles ne contiennent pas de qualificateur [**abstrait**](standard-qualifiers.md) .

Si vous récupérez une classe modifiée à partir d’un espace de noms localisé à l’aide de l’indicateur WBEM \_ \_ utiliser des \_ \_ qualificateurs modifiés et générer une instance à partir de celle-ci, l’instance contient tous les qualificateurs modifiés de la classe modifiée. Vous ne pouvez pas stocker cette nouvelle classe dans l’espace de noms qui contient la définition de classe de base, sauf si vous effectuez l’opération **put** avec l’indicateur WBEM \_ utiliser des \_ \_ \_ qualificateurs modifiés. Cet indicateur demande à WMI de supprimer tous les qualificateurs modifiés avant d’enregistrer l’objet. Si vous ne spécifiez pas \_ d’indicateur WBEM \_ utiliser des \_ \_ qualificateurs modifiés, l’opération **put** échoue avec une erreur d’objet de \_ modification WBEM \_ \_ .

 

 




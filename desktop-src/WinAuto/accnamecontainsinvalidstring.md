---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681f9829f3675c469801e8f40325e83865e625b5f3496e865d1ec383c033b7f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955979"
---
# <a name="accnamecontainsinvalidstring"></a>AccNameContainsInvalidString

## <a name="text"></a>Texte

accName ne doit pas contenir la chaîne {0}

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Le nom d’un élément contient des caractères non valides (ces caractères sont remplacés par AccChecker). Par exemple, la méthode [**obtenir \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) utilisée pour récupérer le nom MSAA d’un élément retourne une chaîne qui contient des caractères de tabulation, de saut de ligne ou de caractère.

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément peut avoir un nom non significatif et non intuitif.

## <a name="possible-causes"></a>Causes possibles

Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriété Name](name-property.md)
</dt> </dl>

 

 





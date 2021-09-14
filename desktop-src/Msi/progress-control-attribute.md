---
description: Cet attribut mesure le remplissage de la barre de l’indicateur de progression.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Progress (attribut de contrôle)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021275"
---
# <a name="progress-control-attribute"></a>Progress (attribut de contrôle)

Cet attribut mesure le remplissage de la barre de l’indicateur de progression. L’enregistrement contient deux entiers et une chaîne. Le premier nombre correspond à la progression, le deuxième nombre à la plage (le nombre maximal possible de la progression). Sur le paramètre, les entiers peuvent être entrés en tant que champs entiers ou chaînes contenant les entiers. Si le deuxième nombre est manquant, il est supposé être la valeur par défaut (1024). Si la progression est supérieure à la plage, elle est remplacée par la plage. Le troisième champ est une chaîne, le nom de l’action dont la progression est affichée.

Pour obtenir des informations connexes, consultez [création d’un contrôle ProgressBar](authoring-a-progressbar-control.md)et [Ajout d’actions personnalisées au ProgressBar](adding-custom-actions-to-the-progressbar.md).

## <a name="valid-controls"></a>Contrôles valides

[ProgressBar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Indicateurs binaires associés

Cet attribut n’utilise pas d’indicateurs binaires.

## <a name="remarks"></a>Notes

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 




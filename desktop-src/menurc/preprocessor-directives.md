---
title: Directives de préprocesseur (menus et autres ressources)
description: Vous pouvez utiliser les directives décrites dans le tableau suivant en fonction des besoins dans votre script de ressources. Ils indiquent à RC d’effectuer des actions ou d’assigner des valeurs à des noms.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- compilateur de ressources, directives de préprocesseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317073"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a>Directives de préprocesseur (menus et autres ressources)

Vous pouvez utiliser les directives décrites dans le tableau suivant en fonction des besoins dans votre script de ressources. Ils indiquent à RC d’effectuer des actions ou d’assigner des valeurs à des noms.



| Directive                     | Description                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [**\#définition**](-define.md)   | Définit un nom spécifié en lui assignant une valeur donnée.               |
| [**\#elif**](-elif.md)       | Marque une clause facultative d’un bloc de compilation conditionnelle.          |
| [**\#else**](-else.md)       | Marque la dernière clause facultative d’un bloc de compilation conditionnelle.    |
| [**\#endif**](-endif.md)     | Marque la fin d’un bloc de compilation conditionnelle.                     |
| [**\#que**](-if.md)           | Compile conditionnellement le script si une expression spécifiée a la valeur true.  |
| [**\#ifdef**](-ifdef.md)     | Compile conditionnellement le script si un nom spécifié est défini.     |
| [**\#ifndef**](-ifndef.md)   | Compile conditionnellement le script si un nom spécifié n’est pas défini. |
| [**\#inclusion**](-include.md) | Copie le contenu d’un fichier dans le fichier de définition de ressource.      |
| [**\#undef**](-undef.md)     | Supprime la définition du nom spécifié.                         |



 

Pour définir des symboles pour vos identificateurs de ressource, utilisez la directive **\# define** pour les définir dans un fichier d’en-tête. Incluez cet en-tête dans le script de ressources et le code source de votre application. De même, vous définissez les valeurs des attributs de ressource et des styles en incluant Windows. h dans le script de ressources.

RC traite les fichiers avec les extensions. c et. h d’une manière spéciale. Il part du principe qu’un fichier avec l’une de ces extensions ne contient pas de ressources. Si un fichier a l’extension de nom de fichier. c ou. h, RC ignore toutes les lignes du fichier, à l’exception des directives de préprocesseur. Par conséquent, pour inclure un fichier qui contient des ressources dans un autre script de ressources, indiquez au fichier d’inclure une extension autre que. c ou. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives pragma](pragma-directives.md)
</dt> </dl>

 

 





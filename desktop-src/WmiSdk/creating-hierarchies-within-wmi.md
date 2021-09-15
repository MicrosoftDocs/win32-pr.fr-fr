---
description: L’espace de noms WMI est un objet de programmation qui définit la portée d’un ensemble de classes et d’instances. Les classes du fournisseur WMI doivent être définies à l’intérieur d’un espace de noms.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Création de hiérarchies dans WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404359"
---
# <a name="creating-hierarchies-within-wmi"></a>Création de hiérarchies dans WMI

L' [*espace de noms WMI*](gloss-n.md) est un objet de programmation qui définit la portée d’un ensemble de classes et d’instances. Les classes du fournisseur WMI doivent être définies à l’intérieur d’un espace de noms.

Les espaces de noms décrivent différents environnements gérés, tels que l’environnement SMS. Étant donné que les classes et les instances d’un schéma définissent les composants d’un environnement managé, chaque nouveau schéma requiert un nouvel espace de noms. Par exemple, l' \\ espace de noms CIMV2 racine contient les classes et les instances définies dans le schéma Win32, ainsi que les classes parent Common Information Model (CIM) dont hérite le schéma Win32. Les classes CIM sont définies par la[DMTF](https://www.dmtf.org/home)(Distributed Management Task Force).

> [!Note]  
> Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction [**\# pragma AutoRecover**](pragma-autorecover.md) de préprocesseur dans votre fichier [*format MOF (MOF)*](gloss-m.md) .

 

WMI définit un espace de noms en tant qu’instance de la classe système d' [**\_ \_ espace de noms**](--namespace.md) ou toute classe qui dérive de l’espace de **\_ \_ noms**. La classe de système d' **\_ \_ espace de noms** a une propriété unique appelée **Name**, qui doit être unique dans l’étendue de l’espace de noms parent. La propriété **Name** doit également contenir une chaîne qui commence par une lettre. Tous les autres caractères de la chaîne peuvent être des lettres, des chiffres ou des traits de soulignement. Tous les caractères ne respectent pas la casse.

En plus de déterminer le nom unique d’un espace de noms enfant, l’espace de noms WMI parent peut protéger les instances statiques de vos classes contre les modifications accidentelles d’autres fournisseurs. Par exemple, il peut s’avérer pratique d’imbriquer un nouvel espace de noms sous un espace de noms existant pour un autre fournisseur. Toutefois, le fournisseur d’origine peut tenter de mettre à jour toutes les instances de classe pour qu’elles correspondent à un nouveau schéma. Dans ce cas, le fournisseur d’origine peut supprimer tous les sous-enfants d’un espace de noms. Bien qu’il s’agit d’une action appropriée pour l’espace de noms cible, elle peut affecter les instances de classe non liées dans un espace de noms enfant (c’est-à-dire vos propres classes de fournisseur).

Par conséquent, il est généralement recommandé de créer et d’enregistrer votre espace de noms séparément des espaces de noms que vous ne contrôlez pas directement. Cela est particulièrement vrai si vos classes dérivent uniquement de classes CIM générales ou d’autres classes de votre entreprise. Votre espace de noms peut être sous l’espace de noms **racine** , comme suit :

**Root/myCompany/myProduct**

En revanche, si votre nouvelle classe dérive de la classe d’un autre fournisseur, vous devrez peut-être stocker votre classe dans un sous-espace de noms de ce fournisseur. Notez que cela expose votre nouvelle classe à une suppression accidentelle par le fournisseur d’origine.

WMI offre plusieurs méthodes différentes pour créer un espace de noms :

-   [Création d’un espace de noms enfant avec du code MOF](creating-a-child-namespace-with-mof-code.md)
-   [Création d’un espace de noms frère avec du code MOF](creating-a-sibling-namespace-with-mof-code.md)
-   [Création d’un espace de noms avec l’API WMI](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 




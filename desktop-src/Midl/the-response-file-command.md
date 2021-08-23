---
title: Commande fichier réponse
description: Un fichier réponse est un fichier texte contenant une ou plusieurs options de ligne de commande du compilateur MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- Référence de ligne de commande MIDL, commande de fichier réponse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c40d8f4255b15a7b95b9bdca9e72ae2cba8e7ea1d42281f441326090a9529d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013527"
---
# <a name="the-response-file-command"></a>Commande fichier réponse

Un fichier réponse est un fichier texte contenant une ou plusieurs options de ligne de commande du compilateur MIDL. Contrairement à une ligne de commande, un fichier réponse autorise plusieurs lignes d’options et de noms de fichiers. Cela peut être utile en raison des limitations de votre environnement de génération ou de la commodité de votre processus de génération.

## <a name="switch-options"></a>Options de commutateur

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*\_fichier réponse*
</dt> <dd>

Spécifie le nom d’un fichier réponse. Le nom du fichier réponse doit suivre immédiatement le caractère @. Aucun espace blanc n’est autorisé entre le caractère @ et le nom du fichier réponse.

</dd> </dl>

## <a name="remarks"></a>Remarques

Au lieu de placer toutes les options associées à un commutateur sur la ligne de commande, le compilateur MIDL accepte les fichiers réponse qui contiennent des commutateurs et des arguments. Les options d’un fichier réponse sont interprétées comme si elles étaient présentes à cet emplacement dans la ligne de commande MIDL.

Chaque argument d’un fichier réponse doit commencer et se terminer sur la même ligne. La barre oblique inverse ( \\ ) ne peut pas être utilisée pour concaténer des lignes. Lorsqu’il fait partie d’une chaîne entre guillemets dans le fichier réponse, la barre oblique inverse peut uniquement être utilisée avant une autre barre oblique inverse ou avant un caractère guillemet double ("). Lorsqu’il ne fait pas partie d’une chaîne entre guillemets, la barre oblique inverse ne peut être utilisée qu’avant un guillemet double.

MIDL prend en charge les arguments de ligne de commande qui incluent un ou plusieurs fichiers réponse associés à d’autres commutateurs de ligne de commande.

Le compilateur MIDL ne prend pas en charge les fichiers réponse imbriqués.

## <a name="examples"></a>Exemples

**compilateur @midl.rsp**

**MIDL-Oicf @midl1.rsp -env Win32 @midl2.rsp ITF. idl**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





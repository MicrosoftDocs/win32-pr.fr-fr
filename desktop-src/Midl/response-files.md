---
title: Fichiers réponse
description: Au lieu de placer toutes les options sur la ligne de commande, le compilateur MIDL accepte les fichiers réponse qui contiennent des commutateurs et des arguments.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL du compilateur MIDL, fichiers réponse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd949a3704b0669fd37c5629307a59df9742010
ms.sourcegitcommit: ad8bd914e19508a67af232d8d59c0e0ee9c3948b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2019
ms.locfileid: "104380466"
---
# <a name="response-files"></a>Fichiers réponse

Au lieu de placer toutes les options sur la ligne de commande, le compilateur MIDL accepte les fichiers réponse qui contiennent des commutateurs et des arguments. Un fichier réponse est un fichier texte contenant une ou plusieurs options de ligne de commande du compilateur MIDL. Contrairement à une ligne de commande, un fichier réponse autorise plusieurs lignes d’options et de noms de fichiers. Cela peut être utile en raison des limitations de votre environnement de génération ou de la commodité pour votre processus de génération. Vous pouvez spécifier un fichier réponse MIDL comme suit :

 **\@ nom de fichier** MIDL

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Spécifie le nom du fichier réponse. Le nom du fichier réponse doit immédiatement suivre le caractère @ sans espace blanc entre le caractère @ et le nom du fichier réponse.

</dd> </dl>

Les options d’un fichier réponse sont interprétées comme si elles étaient présentes à cet emplacement dans la ligne de commande MIDL. Chaque argument d’un fichier réponse doit commencer et se terminer sur la même ligne. Vous ne pouvez pas utiliser la barre oblique inverse ( \) pour concaténer des lignes.

MIDL prend en charge les arguments de ligne de commande qui incluent un ou plusieurs fichiers réponse, associés à d’autres commutateurs de ligne de commande :

**MIDL-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**

Le compilateur MIDL ne prend pas en charge les fichiers réponse imbriqués.

 

 





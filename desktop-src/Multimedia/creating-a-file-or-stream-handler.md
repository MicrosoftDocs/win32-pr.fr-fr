---
title: Création d’un gestionnaire de fichiers ou de flux
description: Création d’un gestionnaire de fichiers ou de flux
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368239"
---
# <a name="creating-a-file-or-stream-handler"></a>Création d’un gestionnaire de fichiers ou de flux

Dans une application écrite dans le langage de programmation C, un gestionnaire de fichiers ou de flux crée généralement une fonction pour chaque méthode. Votre application accède à ces fonctions par le biais d’un tableau de pointeurs de fonction créés par le gestionnaire de flux. Une structure **IAVIStreamVtbl** contient le tableau de pointeurs de fonction. Un gestionnaire de flux peut assigner n’importe quel nom à des fonctions qu’il crée pour les méthodes. La position du pointeur de fonction dans la structure implique la correspondance entre la fonction et la méthode. Par exemple, le premier pointeur de fonction de la structure correspond à la méthode **QueryInterface** . Votre gestionnaire de flux doit fournir toutes les fonctions d’une interface.

 

 





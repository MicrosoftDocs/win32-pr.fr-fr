---
title: Recherche de fichiers
description: Par défaut, RC recherche d’abord les fichiers d’en-tête et les fichiers de ressources (tels que les fichiers icône et curseur) dans le répertoire actif, puis dans les répertoires spécifiés par la variable d’environnement INCLUDe.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294139"
---
# <a name="searching-for-files"></a>Recherche de fichiers

Par défaut, RC recherche d’abord les fichiers d’en-tête et les fichiers de ressources (tels que les fichiers icône et curseur) dans le répertoire actif, puis dans les répertoires spécifiés par la variable d’environnement INCLUDe. (La variable d’environnement PATH n’a aucun effet sur les recherches de répertoires RC.)

## <a name="adding-a-directory-to-search"></a>Ajout d’un répertoire dans lequel effectuer la recherche

Vous pouvez utiliser l’option **/i** pour ajouter un répertoire à la liste des recherches de répertoires RC. Le compilateur recherche ensuite dans les répertoires dans l’ordre suivant :

1.  Répertoire actif
2.  Le ou les répertoires que vous spécifiez à l’aide de l’option **/i** , dans l’ordre dans lequel ils apparaissent sur la ligne de commande RC
3.  Liste des répertoires spécifiés par la variable d’environnement INCLUDe, dans l’ordre dans lequel la variable les répertorie, sauf si vous spécifiez l’option **/x**

L’exemple suivant compile le fichier de définition de ressource MyApp. RC :

**RC/i c : \\ source \\ Stuff/i d : \\ ressources MyApp. RC**

Lors de la compilation du script MyApp. RC, RC recherche d’abord les fichiers d’en-tête et les fichiers de ressources dans le répertoire actif, puis dans C : \\ source \\ Stuff et D : Resources \\ , puis dans les répertoires spécifiés par la variable d’environnement include.

## <a name="ignoring-the-include-environment-variable"></a>La variable d’environnement INCLUDe est ignorée

Vous pouvez empêcher RC d’utiliser la variable d’environnement INCLUDe lors de la détermination des répertoires dans lesquels effectuer la recherche. Pour ce faire, utilisez l’option **/x** . Le compilateur recherche ensuite des fichiers uniquement dans le répertoire actif et dans les répertoires que vous spécifiez à l’aide de l’option **/i** .

La commande suivante compile le fichier de script MyApp. RC :

**RC/x/i c : \\ source source \\ MyApp. RC**

Lors de la compilation du script MyApp. RC, RC recherche d’abord les fichiers d’en-tête et les fichiers de ressources dans le répertoire actif, puis dans C : \\ source \\ . Elle ne recherche pas dans les répertoires spécifiés par la variable d’environnement INCLUDe.

 

 





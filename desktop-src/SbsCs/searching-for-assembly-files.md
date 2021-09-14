---
description: Recherche de fichiers d’assembly
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: Recherche de fichiers d’assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7be73b162ea41fd9eeb0a042a1fc2e202b8115
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121221"
---
# <a name="searching-for-assembly-files"></a>Recherche de fichiers d’assembly

Les contextes d’activation peuvent aider le chargeur à rechercher des fichiers d’assembly. Lorsque le chargeur recherche un fichier à charger par nom, il recherche d’abord des fichiers portant le nom spécifié qui sont référencés par des assemblys qui sont membres du contexte d’activation actuellement actif. Un appel à [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) localise également ces fichiers en premier. Les fichiers ayant le nom spécifié et le contexte d’activation actuel sont trouvés et chargés avant les fichiers portant le nom dans le répertoire local ou dans la variable d’environnement PATH. Cela signifie que lorsque vous créez des manifestes, vous devez répertorier tous les fichiers que vous prévoyez d’utiliser avec **SearchPath**, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)ou les importations statiques.

Notez que ces fichiers ne sont pas automatiquement localisés lors de l’utilisation de [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou d’autres fonctions qui ne recherchent pas de fichiers. Pour utiliser ces fichiers avec **CreateFile**, utilisez d’abord [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) pour rechercher le chemin d’accès au fichier isolé, puis utilisez **CreateFile** sur le chemin d’accès retourné.

Cette méthode de recherche de fichiers permet de séparer les applications isolées, car plusieurs fichiers portant le même nom peuvent différer uniquement par leur association à des assemblys de numéros de version différents. Le système d’exploitation peut trouver le fichier approprié à utiliser pendant les opérations sur les fichiers.

Si une DLL est chargée de cette manière à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya), le point d’entrée de cette dll (DllMain) est appelé alors que le contexte d’activation d’origine est maintenu actif, sauf si la dll elle-même contient un manifeste à un ID de ressource spécifique ( \_ ID de ressource de manifeste ISOLATIONAWARE \_ \_ , ou 2)

 

 

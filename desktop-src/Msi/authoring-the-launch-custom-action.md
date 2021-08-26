---
description: le code source d’un exemple d’action personnalisée nommé Launch, qui répond aux exemples de spécifications, est fourni par le kit de développement logiciel (SDK) Windows Installer en tant que fichier Tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Création de l’action personnalisée de lancement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536f22c95d871ab502518a0619efad5ae70cb348cdf75163fc50309b440f6393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045271"
---
# <a name="authoring-the-launch-custom-action"></a>Création de l’action personnalisée de lancement

le code source d’un exemple d’action personnalisée nommé Launch, qui répond aux exemples de spécifications, est fourni par le kit de développement logiciel (SDK) Windows Installer en tant que fichier Tutorial. cpp. Cette action personnalisée utilise [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) pour mettre en forme une chaîne contenant des propriétés. La propriété \[ \# FileKey \] correspond au chemin d’accès complet du fichier html. Utilisez le fichier source pour créer le fichier Tutorial.dll. Le point d’entrée de cette DLL est LaunchTutorial.

L’exemple d’action personnalisée Launch appelle une DLL écrite en C++ et est générée à partir d’un flux binaire temporaire. Les actions personnalisées de ce type incluent les constantes de type de base msidbCustomActionTypeDll et msidbCustomActionTypeBinaryData, qui donnent un type numérique de base égal à 1. Consultez [type d’action personnalisée 1](custom-action-type-1.md). Étant donné que les spécifications requièrent que l’installation se poursuive en cas d’échec de l’action personnalisée, Launch comprend également la constante facultative **msidbCustomActionTypeContinue**, qui est 64. Consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md). Le type numérique total du lancement est 65.

Continuez à [Ajouter le lancement aux tables CustomAction et binaires](adding-launch-to-the-customaction-and-binary-tables.md).

 

 




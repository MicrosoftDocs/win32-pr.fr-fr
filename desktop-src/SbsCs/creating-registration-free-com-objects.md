---
description: Les contextes d’activation permettent d’utiliser des objets COM sans qu’il soit nécessaire de les inscrire.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Création d’objets Registration-Free COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238074"
---
# <a name="creating-registration-free-com-objects"></a>Création d’objets Registration-Free COM

Les contextes d’activation permettent d’utiliser des objets COM sans qu’il soit nécessaire de les inscrire. Cela permet à votre application d’avoir plusieurs composants avec des fonctionnalités différentes en fonction de leur version plutôt que de leurs informations de registre. Plusieurs composants peuvent exposer le même objet COM avec le même GUID, mais ont des fonctionnalités différentes en fonction de la version.

Quand une application demande un GUID à partir de [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid), com commence par Rechercher le mappage du ProgID au CLSID dans le contexte d’activation actif. Quand une application utilise [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un pointeur d’interface d’instance, com recherche dans le contexte d’activation actif pour déterminer quelle dll hébergera le CLSID. Si le contexte d’activation ne contient pas les informations requises, COM recherche les informations dans le registre à l’aide de la méthode habituelle.

Notez que, étant donné que les contextes d’activation sont par thread, COM marshale le contexte d’activation du thread de création sur le thread hôte et l’active avant d’appeler [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) sur le thread hôte. cette fonctionnalité est déjà présente dans Windows, le code client n’est pas obligé de faire quoi que ce soit pour l’implémenter.

Les classes COM peuvent être exportées par des composants hébergés sans passer par le registre. Plusieurs composants peuvent exposer le même ProgID pour différents objets COM, et votre application d’hébergement doit uniquement trouver le contexte d’activation approprié, puis utiliser [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir les pointeurs d’interface de l’objet hébergé.

 

 

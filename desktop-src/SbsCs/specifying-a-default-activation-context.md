---
description: Spécification d’un contexte d’activation par défaut
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Spécification d’un contexte d’activation par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1598e0a111b358a783b940a5c036d63eef348740ff2467d3ed78720c6a5210
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977139"
---
# <a name="specifying-a-default-activation-context"></a>Spécification d’un contexte d’activation par défaut

lorsque votre application ou composant crée un nouveau processus, Windows recherche un manifeste d’application par défaut. Notez qu’un manifeste inclus en tant que ressource dans l’application est prioritaire par rapport à un manifeste externe. Le contexte d’activation par défaut est le premier contexte d’activation qui est actif avant l’activation d’un autre contexte d’activation. Ce contexte d’activation est toujours actif, sauf si vous activez d’autres contextes. Si vous définissez \_ la prise \_ en charge de l’isolation activée quand vous compilez votre application ou composant, les appels tels que [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)et [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) peuvent effectuer la gestion de contexte automatique.

Le chargeur permet à une application de spécifier son contexte d’activation par défaut à l’aide de deux méthodes. Vous pouvez placer le fichier manifeste dans les ressources de l’exécutable et le chargeur le trouvera. Cela revient à placer le fichier manifeste dans la table de ressources de l’exécutable. Vous pouvez placer le manifeste dans un fichier nommé *Myapp*.exe. Manifeste dans le même répertoire que *myapp*.exe, et le chargeur le trouve lors de la recherche d’une.exe *MyApp* .

Si vous n’utilisez aucune de ces méthodes, l’application démarre avec le contexte d’activation par défaut du système, qui contient un ensemble minimal d’assemblys.

Une meilleure façon d’utiliser la gestion de contexte automatique consiste à compiler votre application avec la prise en charge de l’ISOLATION \_ \_ activée définie. La méthode recommandée consiste à définir cela sur la ligne de commande du compilateur pour l’ensemble du projet en cours de génération, plutôt que de les définir dans des en-têtes ou des fichiers sources individuels. Cela permet à la plupart des API Win32 d’être conscientes des contextes d’activation et de savoir comment les gérer. Au lieu d’avoir à effectuer votre propre gestion du contexte d’activation, vous devez simplement placer un manifeste dans votre table de ressources au niveau de l’ID de ressource ISOLATIONAWARE \_ manifeste \_ \_ ID de ressource (valeur numérique 2), de type RT \_ Manifest (valeur numérique 24). Des fonctions telles que [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)et [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) activent ensuite automatiquement ce contexte avant d’effectuer l’appel réel.

Notez que si vous compilez avec la prise en \_ charge de \_ l’isolation activée, vous ne pouvez pas également effectuer votre propre gestion du contexte d’activation. lorsque l' \_ option prise en charge de \_ l’ISOLATION est définie, Windows ignore toute création de contexte d’activation dynamique que votre application peut tenter d’effectuer entre les appels [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) et [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . Cela signifie que lorsque votre application utilise la prise en charge de l’ISOLATION \_ \_ activée, vous devez vous assurer que le manifeste contient une liste complète de tous les assemblys requis par votre composant.

 

 

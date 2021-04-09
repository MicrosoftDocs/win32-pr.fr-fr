---
description: Les tables de messages sont des ressources de chaîne spéciales utilisées lors de l’affichage des messages d’erreur. Ils sont déclarés dans un fichier de ressources à l’aide de l’instruction de définition de ressource MESSAGETABLE. Pour accéder aux chaînes de message, utilisez la fonction FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tables de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950439"
---
# <a name="message-tables"></a>Tables de messages

Les tables de messages sont des ressources de chaîne spéciales utilisées lors de l’affichage des messages d’erreur. Ils sont déclarés dans un fichier de ressources à l’aide de l’instruction de définition de ressource [MESSAGETABLE](../menurc/messagetable-resource.md) . Pour accéder aux chaînes de message, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .

Le système fournit une table de messages pour les [codes d’erreur système](system-error-codes.md). Pour récupérer la chaîne qui correspond au code d’erreur, appelez [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système.

Pour fournir une table de messages pour votre application, suivez les instructions figurant dans [fichiers texte du message](../eventlog/message-text-files.md). Pour récupérer des chaînes à partir de votre table de messages, appelez [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec l’indicateur formater le \_ message \_ de \_ HMODULE.

 

 

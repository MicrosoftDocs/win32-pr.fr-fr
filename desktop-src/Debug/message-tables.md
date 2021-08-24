---
description: Les tables de messages sont des ressources de chaîne spéciales utilisées lors de l’affichage des messages d’erreur. Ils sont déclarés dans un fichier de ressources à l’aide de l’instruction de définition de ressource MESSAGETABLE. Pour accéder aux chaînes de message, utilisez la fonction FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tables de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6141f78342db2554e85053adda7ee68bdb0e855f213f103da1bb7f62eac1d703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691819"
---
# <a name="message-tables"></a>Tables de messages

Les tables de messages sont des ressources de chaîne spéciales utilisées lors de l’affichage des messages d’erreur. Ils sont déclarés dans un fichier de ressources à l’aide de l’instruction de définition de ressource [MESSAGETABLE](../menurc/messagetable-resource.md) . Pour accéder aux chaînes de message, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .

Le système fournit une table de messages pour les [codes d’erreur système](system-error-codes.md). Pour récupérer la chaîne qui correspond au code d’erreur, appelez [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système.

Pour fournir une table de messages pour votre application, suivez les instructions figurant dans [fichiers texte du message](../eventlog/message-text-files.md). Pour récupérer des chaînes à partir de votre table de messages, appelez [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec l’indicateur formater le \_ message \_ de \_ HMODULE.

 

 

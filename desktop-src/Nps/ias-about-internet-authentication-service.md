---
title: À propos des extensions NPS
description: Cette section décrit comment implémenter des dll pour étendre les fonctionnalités du serveur NPS. Il décrit l’interaction entre NPS et les dll, et présente des considérations de conception concernant les dll.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513729"
---
# <a name="about-nps-extensions"></a>À propos des extensions NPS

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

Cette section décrit comment implémenter des dll pour étendre les fonctionnalités du serveur NPS. Il décrit l’interaction entre NPS et les dll, et présente des considérations de conception concernant les dll.

NPS fournit deux points d’extension, un pour l’authentification et l’autre pour l’autorisation. L’authentification fait référence à la vérification de l’identité de l’utilisateur. L’autorisation fait référence à la détermination des services que le réseau doit fournir à l’utilisateur. Les deux points d’extension correspondent aux DLL d’extension d’authentification et aux DLL d’extension d’autorisation. Chaque point d’extension peut prendre en charge plusieurs dll.

NPS fournit des services d’authentification et d’autorisation. Les dll d’extension d’authentification sont appelées par NPS avant l’authentification et l’autorisation intégrées du serveur NPS. Les dll d’extension d’autorisation sont appelées après l’authentification et l’autorisation du serveur NPS.

Le diagramme suivant illustre le déroulement des paquets via un serveur RADIUS NPS développé à l’aide de DLL d’extension.

![processus d’authentification et d’autorisation du serveur NPS](images/ias03.png)

Si une DLL d’extension d’authentification retourne ACCEPT, le paquet ignore l’authentification NPS et passe directement à l’autorisation NPS.

> [!Note]  
> Lorsque plusieurs DLL d’extension d’authentification sont présentes, le reste des dll d’extension peut également être ignoré. Pour plus d’informations, consultez [Configuration des dll d’extension](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .

 

Si une DLL d’extension d’authentification retourne CONTINUE, le paquet passe à l’authentification NPS, puis à l’autorisation NPS.

> [!Note]  
> Lorsque plusieurs DLL d’extension d’authentification sont présentes, le reste des dll d’extension d’authentification est appelé avant l’authentification NPS.

 

Les rubriques suivantes décrivent plus en détail les dll d’extension :

-   [Configuration des dll d’extension](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [Appel des dll d’extension](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [Attributs d’identification utilisateur](/windows/desktop/Nps/ias-user-identification-attributes)

 

 
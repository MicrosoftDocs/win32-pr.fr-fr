---
title: Attributs d’identification utilisateur
description: L’identité de l’utilisateur demandant l’authentification est fournie aux DLL d’extension NPS dans plusieurs attributs différents.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Attributs, identification de l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511090"
---
# <a name="user-identification-attributes"></a>Attributs d’identification utilisateur

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

L’identité de l’utilisateur demandant l’authentification est fournie aux DLL d’extension NPS dans plusieurs attributs différents.

-   **ratUserName**
-   **ratStrippedUserName**
-   **ratFQUserName**

Chaque attribut fournit l’identité de l’utilisateur dans un format différent. En général, les développeurs doivent utiliser **ratStrippedUserName**. Les utilisations des attributs **ratUserName** et **ratFQUserName** sont plus spécialisées.

> [!Note]  
> L’attribut User-Password, **ratUserPassword**, a déjà été déchiffré lorsqu’il est envoyé à la dll d’extension et est utilisable sous cette forme.

 

## <a name="ratusername"></a>ratUserName

L’attribut **ratUserName** contient le nom qui a été réellement envoyé « sur le réseau ». NPS n’a pas, de quelque manière, traité ni validé le contenu de cet attribut. Cet attribut n’est peut-être pas disponible du tout car l’utilisateur a peut-être été identifié par un moyen tel que ID de l’appelant.

Lors de l’utilisation de [**RadiusExtensionProcess/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), si cet attribut est disponible, il est disponible uniquement au point de plug-in de DLL d’extension d’authentification. L’attribut **ratUserName** n’est pas disponible sur le point de plug-in de DLL d’extension d’autorisation, car dans les dll d’extension d’autorisation les fonctions **RadiusExtensionProcess/ex** affichent uniquement les attributs « sortants ».

Quand vous utilisez [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), si cet attribut est disponible, il est disponible à la fois dans le point de plug-in de DLL d’extension d’authentification et dans le point de plug-in de DLL d’extension d’autorisation.

## <a name="ratstrippedusername"></a>ratStrippedUserName

Le **ratStrippedUserName** est l’identité de l’utilisateur après « suppression du domaine ». Pour plus d’informations sur la suppression de domaines, consultez la rubrique relative aux [noms de domaine](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) sur http : \\ \\ technet2.Microsoft.com.

Cet attribut peut être présent au point de plug-in de DLL d’extension d’authentification, au point de plug-in DLL d’extension d’autorisation ou aux deux. Le format de cet attribut est garanti :

****\\*** Nom d’utilisateur du domaine*

Où *domaine* est le nom de domaine NetBIOS.

## <a name="ratfqusername"></a>ratFQUserName

L’attribut **ratFQUserName** est le nom d’utilisateur « complet ».

Cet attribut peut être présent dans le point de plug-in de DLL d’extension d’authentification, le point de plug-in DLL d’extension d’autorisation, ou les deux. Toutefois, le format de l’attribut peut varier entre les deux points de plug-in. Au point de plug-in de DLL d’extension d’authentification, cet attribut aura toujours la forme suivante :

****\\*** Nom d’utilisateur du domaine*

Le format de l’attribut **ratFQUserName** au point de plug-in de DLL d’extension d’autorisation varie selon que l’utilisateur est un utilisateur Active Directory.

-   Si l’utilisateur est un utilisateur local, **ratFQUserName** a le même format que pour le point de plug-in de DLL d’extension d’authentification :

    ****\\*** Nom d’utilisateur du domaine*

    .

-   Si l’utilisateur est un utilisateur Active Directory, **ratFQUserName** peut contenir le nom de l’utilisateur au format « canonique ». Le format canonique est le format utilisé par le Active Directory pour identifier l’utilisateur. Il s’agit du chemin d’accès à la racine de l’arborescence de Active Directory et comprend l’unité d’organisation de l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration des dll d’extension](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Appel des dll d’extension](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 
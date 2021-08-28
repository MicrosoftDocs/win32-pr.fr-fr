---
title: Appel de WDS à partir de pages Web
description: vous pouvez appeler Microsoft Windows Desktop Search (WDS) à partir de n’importe quelle page web que vous créez ou gérez à l’aide de l’objet d’assistance du navigateur (BHO) et d’Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac2be6be30889e8f759ee3cf7529250a5513ce58
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883703"
---
# <a name="calling-wds-from-web-pages"></a>Appel de WDS à partir de pages Web

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

vous pouvez appeler Microsoft Windows Desktop Search (WDS) à partir de n’importe quelle page web que vous créez ou gérez à l’aide de l’objet d’assistance du navigateur (BHO) et d’Windows Internet Explorer. Vous pouvez voir comment cela fonctionne sur la page Web MSN. Au-dessus de la zone de recherche de https://www.msn.com se trouvent plusieurs types de recherche : Web, Actualités, images, Desktop, Encarta et local. si vous cliquez sur bureau, les paramètres de recherche sont transmis à Windows desktop search, qui recherche le catalogue et affiche les résultats dans l’interface utilisateur WDS. Pour que les utilisateurs puissent démarrer une recherche sur le Bureau à partir de vos pages Web, WDSBHO doit être installé et activé sur leurs systèmes, vos pages Web doivent être inscrites auprès de WDS en tant qu’URL autorisée, et vous devez créer un lien pour transmettre la requête enetered utilisateur à WDS.

## <a name="enabling-the-wds-browser-help-object"></a>Activation de l’objet d’aide du navigateur WDS

L’BHO est installé et activé par défaut dans Internet Explorer lorsque vous installez WDS, mais vous pouvez facilement vérifier qu’il n’a pas été désactivé ou désinstallé. Sur le système d’un utilisateur, ouvrez Internet Explorer, sélectionnez **Options Internet** dans le menu **Outils** , cliquez sur l’onglet **programmes** , puis sur **gérer les modules complémentaires**. Dans la liste des modules complémentaires, recherchez la classe dsWebAllowBHO et assurez-vous qu’elle est activée. Lorsque l’BHO est désactivé, WDS continue de fonctionner normalement. Toutefois, vous ne pourrez pas effectuer de recherches sur le Bureau à partir d’une page Web.

Les deux options suivantes pour autoriser une recherche sur le bureau exécutent la recherche localement avec l’application de recherche inscrite.

## <a name="registering-web-page-urls"></a>Inscription des URL de page Web

Le registre contient une liste d’URL de domaine « autorisées » à partir desquelles WDS peut être appelé. Pour inclure vos pages Web, vous devez répertorier votre ou vos URL de domaine en tant que REG \_ SZ dans le registre comme suit :

**HKEY \_ \_ordinateur LOCAL** \\ **logiciel** \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **autorisé** \\ *&lt; nombre &gt;*  =  &lt; domainURL&gt;

Où **&lt; Number &gt;** est numéroté séquentiellement et **&lt; DomainURL &gt;** est l’URL de la page Web à partir de laquelle vous souhaitez autoriser les recherches WDS. Cette chaîne d’URL peut inclure l’astérisque générique \* au début ou à la fin de l’URL. Par exemple, si la chaîne est « \* . mydomain.com », vous pouvez démarrer une recherche WDS à partir de https://www.mydomain.com et de https://mydomain.com .

## <a name="enabling-desktop-search-by-url"></a>Activation de Desktop Search by URL

Une autre option qui ne nécessite pas l’accès au registre consiste à utiliser l’URL suivante sur vos pages Web :

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

où **requête** est la chaîne encodée URL sur laquelle l’utilisateur recherche, y compris les termes de la [syntaxe de requête avancée](-search-2x-wds-aqsreference.md) .

 

 





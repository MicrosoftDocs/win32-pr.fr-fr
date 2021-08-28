---
title: Accès au contrôle dans les pages Web
description: Accès au contrôle dans les pages Web
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb6476ebdf2d26f1aec12a2f46506b3c4882d06
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882971"
---
# <a name="accessing-the-control-in-web-pages"></a>Accès au contrôle dans les pages Web

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Pour accéder aux services Microsoft Agent à partir d’une page Web, utilisez la &lt; &gt; balise d’objet HTML dans le <HEAD> ou &lt; &gt; élément Body de la page, en spécifiant le CLSID Microsoft (identificateur de classe) pour le contrôle. En outre, utilisez un paramètre CODEBASE pour spécifier l’emplacement du fichier d’installation de l’agent Microsoft et son numéro de version.

Si Microsoft Internet Explorer (version 3,02 ou ultérieure) est installé sur le système, mais que Microsoft Agent n’est pas encore installé et que l’utilisateur accède à une page Web contenant la &lt; &gt; balise d’objet avec le CLSID de l’agent, le navigateur tente automatiquement de télécharger l’agent à partir du site Web de Microsoft. L’utilisateur sera alors invité à confirmer l’installation. pour les autres navigateurs, contactez le fournisseur pour obtenir des informations sur leur support ou un support tiers pour les contrôles de ActiveX.

L’exemple suivant illustre l’utilisation du paramètre CODEBASE pour télécharger la version anglaise (English Language) 2,0 de Microsoft Agent.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Vous pouvez également installer l’agent à partir de votre propre serveur HTTP ou dans le cadre du processus d’installation d’une application. Pour prendre en charge l’installation à partir de votre propre serveur HTTP, vous devez poster le fichier de .Exe CAB de l’agent Microsoft qui s’installe automatiquement et spécifier son URL dans la balise de code base.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Pour prendre en charge le téléchargement automatique d’un composant de langue Microsoft Agent à partir d’une page Web, incluez la balise Object du composant de langue sur la page avant la balise d’objet de contrôle de l’agent :

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

où XXXX est remplacé par un ID de langue. Pour les langues actuellement prises en charge, consultez le site Web de Microsoft Agent.

-   La &lt; &gt; balise Object pour un composant de langage doit précéder la &lt; &gt; balise Object pour le composant principal de Microsoft Agent.
-   Plusieurs langues peuvent être installées sur le même client.
-   Avant de définir l' [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) d’un caractère, nous vous recommandons de vérifier que les paramètres régionaux du navigateur, disponibles dans la propriété [**userLanguage**](https://www.bing.com/search?q=**userLanguage**) , correspondent à la langue définie.

Pour prendre en charge d’autres versions linguistiques de l’agent, vous utilisez une autre balise d’objet qui spécifie le composant de langue. Toutefois, sachez que la tentative d’installation de plusieurs langues à la fois peut nécessiter un redémarrage de l’utilisateur. Les composants de langue de l’agent peuvent être obtenus à partir du site Web de l’agent à l’aide de la même procédure que pour le composant principal de l’agent. Les licences de distribution pour les composants de langue sont couvertes dans la licence de distribution d’agent standard. Pour commencer à utiliser un caractère, vous devez charger le caractère à l’aide de la méthode [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) . Un caractère peut être chargé à partir du stockage local de l’utilisateur ou d’un serveur HTTP. Pour plus d’informations sur la syntaxe de chargement d’un caractère, consultez la méthode **Load** . Une fois le caractère correctement chargé, vous pouvez utiliser les méthodes, les propriétés et les événements exposés par le contrôle de l’agent pour programmer le caractère. Vous pouvez également utiliser les méthodes, propriétés et événements exposés par votre langage de programmation et le navigateur pour programmer le caractère. par exemple, pour programmer sa réaction sur un clic de bouton. Consultez la documentation de votre navigateur pour déterminer les fonctionnalités qu’il expose dans son modèle de script. pour Microsoft Internet Explorer, consultez le modèle objet de script, disponible dans le kit de développement logiciel (SDK) ActiveX.

Les services de l’agent restent chargés uniquement lorsqu’il existe au moins une application cliente avec une connexion. Cela signifie que lorsqu’un utilisateur passe d’une page Web à l’autre, l’agent s’arrête et tous les caractères que vous avez chargés disparaissent. Pour maintenir l’exécution de l’agent entre les pages (et donc garder un caractère visible), créez un autre client qui reste chargé entre les modifications de page. Par exemple, vous pouvez créer un jeu de frames HTML et déclarer une &lt; &gt; balise d’objet pour agent dans le frame parent. Vous pouvez ensuite générer un script des pages que vous chargez dans le ou les frames enfants pour appeler le script du parent. Vous pouvez également inclure une &lt; balise d’objet &gt; sur chaque page que vous chargez dans le frame enfant. Dans ce cas, n’oubliez pas que chaque page sera son propre client. Vous devrez peut-être utiliser la méthode [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) pour définir le client qui contrôle le moment où l’utilisateur interagit avec la page parente ou enfant.

 

 

---
description: Par défaut, le module de reconnaissance utilise un dictionnaire système qui contient tous les mots couramment écrits dans une langue.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Utilisation des dictionnaires d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c83013f704fe28b5754ab89fd95ed730e16d1cda5ab257d4fb411d0e7293347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449231"
---
# <a name="using-application-dictionaries"></a>Utilisation des dictionnaires d’applications

Par défaut, le module de reconnaissance utilise un dictionnaire système qui contient tous les mots couramment écrits dans une langue. En outre, le module de reconnaissance possède un dictionnaire utilisateur qui contient des mots que l’utilisateur a ajoutés au dictionnaire. Les utilisateurs ajoutent un mot au dictionnaire de l’utilisateur via le panneau de saisie Tablet PC par le biais de sélections dans :

-   Liste alternative (lors de l’écriture).
-   Le menu Speech Tools (en parlant).

Si vous concevez une application dans laquelle vous prévoyez que l’utilisateur écrira des mots qui ne se trouvent pas dans le dictionnaire système ou le dictionnaire de l’utilisateur, créez un dictionnaire d’applications. Un dictionnaire d’applications améliore la précision de la reconnaissance en fournissant au module de reconnaissance une liste personnalisée de mots susceptibles d’être entrés comme écriture manuscrite dans une application.

Vous créez un dictionnaire d’applications à l' [**aide de l’objet de**](inkwordlist-class.md) la demande. Le dictionnaire d’applications qui en résulte augmente la précision de la reconnaissance en fournissant au module de reconnaissance une liste de mots attendus. Par exemple, un dictionnaire d’applications qui contient une terminologie médicale augmente la précision de la reconnaissance au sein d’une application développée pour l’industrie médicale dans laquelle les termes sont susceptibles d’être écrits.

À titre d’exemple, lors de la conception d’un formulaire pour qu’un utilisateur puisse commander des instruments de musique, créez un objet de la feuille de [**mots**](inkwordlist-class.md) qui contient les noms des fabricants d’instruments les plus courants. Définissez la propriété de la plage de [**mots**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) sur l’objet **de la sorte** que vous avez créé. Cette liste de mots est ensuite transmise à la reconnaissance par l’objet **RecognizerContext** . Le dictionnaire d’applications augmente la précision de la reconnaissance lorsque ces noms sont écrits dans un champ de l’application.

Les rubriques suivantes décrivent comment utiliser les dictionnaires d’applications.

-   [Compréhension des listes de mots, du contexte de reconnaissance et des Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [Utilisation de dictionnaires d’applications avec les API de plateforme Tablet PC](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [Création de dictionnaires personnalisés pour la reconnaissance de l’écriture manuscrite](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 




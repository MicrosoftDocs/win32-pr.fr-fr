---
description: 'Avant de placer des données dans le registre, une application doit diviser les données en deux catégories : données spécifiques à l’ordinateur et données spécifiques à l’utilisateur.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Catégories de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4bf4abb7af2abf723aa42f3426c58230083d8e575dda176b8eeda0daecb36d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885850"
---
# <a name="categories-of-data"></a>Catégories de données

Avant de placer des données dans le registre, une application doit diviser les données en deux catégories : données spécifiques à l’ordinateur et données spécifiques à l’utilisateur. En faisant cette distinction, une application peut prendre en charge plusieurs utilisateurs, tout en trouvant des données spécifiques à l’utilisateur sur un réseau et en utilisant ces données dans différents emplacements, ce qui permet d’obtenir des données de profil utilisateur indépendantes de l’emplacement. (Un profil utilisateur est un ensemble de données de configuration enregistrées pour chaque utilisateur.)

Lorsque l’application est installée, elle doit enregistrer les données spécifiques à l’ordinateur sous la clé de l' **\_ \_ ordinateur local HKEY** . En particulier, il doit créer des clés pour le nom de la société, le nom du produit et le numéro de version, comme indiqué dans l’exemple suivant :

**HKEY \_ \_ \\ Logiciel \\ de l’ordinateur local**_MyCompany \\ MyProduct \\ 1,0_

Si l’application prend en charge COM, elle doit enregistrer ces données sous **HKEY \_ local \_ machine \\ Software \\ classes**.

Une application doit enregistrer des données spécifiques à l’utilisateur sous la clé **HKEY \_ Current \_ User** , comme illustré dans l’exemple suivant :

**HKEY \_ \_ \\ Logiciel \\ utilisateur actuel**_MyCompany \\ MyProduct \\ 1,0_

 

 




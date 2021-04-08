---
title: Assistants de création d’objets
description: Dans les composants logiciels enfichables MMC d’administration de Active Directory Domain Services, l’utilisateur peut créer des objets dans un répertoire en ouvrant le menu contextuel du conteneur dans lequel le nouvel objet sera créé, en choisissant nouveau et en choisissant la classe de l’objet à créer. La création de nouvelles instances d’un objet démarre l’Assistant Création d’objet. Chaque classe d’objet peut spécifier l’utilisation d’un assistant de création spécifique, ou elle peut utiliser un assistant de création générique. Pour les classes courantes, telles que user et organizationalUnit, le composant logiciel enfichable utilisateurs et ordinateurs Active Directory fournit un ensemble standard d’assistants de création. Il existe deux façons d’étendre un Assistant Création remplacer un Assistant existant ou d’en fournir un s’il n’en existe pas pour la classe. l’Assistant existant est remplacé par la création d’une extension de création d’objet primaire. Une extension de création principale fournit le premier ensemble de pages et est hébergée de la même façon que les pages natives. Une extension de création principale prend également en charge le mécanisme d’extensibilité afin que d’autres extensions de l’Assistant Création puissent être appelées. Pour obtenir un exemple d’extension principale, consultez l’exemple scpwizard dans le kit de développement logiciel (SDK) de la plateforme. Étendre un Assistant existant un Assistant existant peut être étendu à l’aide d’une extension de création d’objet secondaire. Une extension de création secondaire ajoute des pages d’assistant aux pages natives ou à l’extension principale. Pour plus d’informations et pour obtenir un exemple d’extension de création secondaire, consultez l’exemple userwizard dans le kit de développement logiciel (SDK) de plateforme.
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- objets Active Directory, assistants de création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc3dbacaf6eee5670fdacd9a587a497397c4d1b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101441"
---
# <a name="object-creation-wizards"></a>Assistants de création d’objets

Dans les composants logiciels enfichables MMC d’administration de Active Directory Domain Services, l’utilisateur peut créer des objets dans un répertoire en ouvrant le menu contextuel du conteneur dans lequel le nouvel objet sera créé, en choisissant **nouveau** et en choisissant la classe de l’objet à créer. La création de nouvelles instances d’un objet démarre l’Assistant Création d’objet. Chaque classe d’objet peut spécifier l’utilisation d’un assistant de création spécifique, ou elle peut utiliser un assistant de création générique. Pour les classes courantes, telles que [**User**](/windows/desktop/ADSchema/c-user) et [**OrganizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit), le composant logiciel enfichable utilisateurs et ordinateurs Active Directory fournit un ensemble standard d’assistants de création.

Il existe deux façons d’étendre un assistant de création :

-   Remplacer un Assistant existant ou en fournir un s’il n’en existe pas pour la classe : l’Assistant existant est remplacé par la création d’une *extension de création d’objet primaire*. Une extension de création principale fournit le premier ensemble de pages et est hébergée de la même façon que les pages natives. Une extension de création principale prend également en charge le mécanisme d’extensibilité afin que d’autres extensions de l’Assistant Création puissent être appelées. Pour obtenir un exemple d’extension principale, consultez l’exemple scpwizard dans le kit de développement logiciel (SDK) de la plateforme.
-   Étendre un Assistant existant : un Assistant existant peut être étendu à l’aide d’une *extension de création d’objet secondaire*. Une extension de création secondaire ajoute des pages d’assistant aux pages natives ou à l’extension principale. Pour plus d’informations et pour obtenir un exemple d’extension de création secondaire, consultez l’exemple userwizard dans le kit de développement logiciel (SDK) de plateforme.

## <a name="developer-audience"></a>Public de développeurs

Cette documentation suppose que le lecteur est familiarisé avec l’opération COM et le développement de composants à l’aide de C++. Il n’est actuellement pas possible de créer une extension à l’Assistant Création d’objet Active Directory à l’aide de Visual Basic.

## <a name="creating-an-active-directory-object-creation-extension"></a>Création d’une extension de création d’objet Active Directory

Les extensions de création d’objets primaires et secondaires sont des serveurs COM in-proc qui implémentent certaines interfaces et sont inscrits auprès de Active Directory Domain Services.

**Pour créer et installer une extension de création d’objet**

1.  Créez la DLL d’extension de création d’objet. Une extension de création d’objet est un serveur COM in-proc qui, au minimum, implémente l’interface [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) . Pour plus d’informations, consultez [implémentation de l’objet com d’extension de création d’objet](implementing-the-object-creation-extension-com-object.md).
2.  Installez l’extension de création sur les ordinateurs où l’extension de création doit être utilisée. Pour ce faire, créez un package de Microsoft Windows Installer pour la DLL d’extension de création et déployez le package de manière appropriée à l’aide de la stratégie de groupe. Pour plus d’informations, consultez distribution des composants de l' [interface utilisateur](distributing-user-interface-components.md).
3.  Enregistrez l’extension de création dans le Registre Windows et avec Active Directory Domain Services. Pour plus d’informations, consultez [inscription de l’extension de création d’objet](registering-the-object-creation-extension.md).

## <a name="using-an-object-creation-wizard"></a>Utilisation d’un assistant de création d’objet

Un assistant de création d’objet peut également être appelé à partir d’une application autre que les composants logiciels enfichables MMC d’administration de Active Directory Domain Services. Pour plus d’informations, consultez [appel de l’Assistant Création à partir de votre application](invoking-creation-wizards-from-your-application.md).

Si un assistant de création n’est pas inscrit pour une classe d’objet, les composants logiciels enfichables d’administration fournissent un Assistant Création générique. L’Assistant Création générique est généré au moment de l’exécution à partir de la liste des propriétés obligatoires de la classe de l’objet créé. Pour chaque propriété obligatoire, une page est ajoutée à l’interface utilisateur. L’Assistant de création générique n’est pas extensible. Si l’extensibilité est requise, elle doit être remplacée par une extension de création d’objet primaire.

 

 
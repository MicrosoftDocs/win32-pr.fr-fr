---
description: Cette rubrique résume les principales considérations en matière de programmation à prendre en compte lors de l’ajout de fonctionnalités MUI à vos applications.
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: Développement d’applications MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a3278b4cc70969c1aa968de895d99fd3363a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867933"
---
# <a name="development-of-mui-applications"></a>Développement d’applications MUI

Cette rubrique résume les principales considérations en matière de programmation à prendre en compte lors de l’ajout de fonctionnalités MUI à vos applications.

## <a name="requirements-for-a-mui-application"></a>Configuration requise pour une application MUI

La fonctionnalité MUI est appliquée uniquement à la localisation d’une application entièrement globalisée, créée à l’aide d’un processus appelé Software internationalisation. Le [Centre de développement Microsoft Go Global](https://msdn.microsoft.com/goglobal) offre une vaste sélection de documentation connexe qui vous permet de concevoir, de créer et de déployer des applications mondialisables. Ces documents vous aident à prendre en compte la façon dont les caractéristiques des différentes langues humaines peuvent affecter la conception de vos logiciels. Notez que le portail fournit également une archive complète des colonnes Dr. international.

Votre application MUI peut s’exécuter dans n’importe quel langage ou paramètre régional, et l’utilisateur peut demander toute langue pour laquelle l’application prend en charge. Par conséquent, l’application doit encoder le texte de l’interface utilisateur pour prendre en charge la variété de langues la plus large possible. La chose la plus importante à retenir est d’utiliser [Unicode](unicode.md) pour gérer l’ensemble du traitement du texte. Pour plus d’informations sur la globalisation à l’aide d’Unicode, consultez le [Centre de développement Microsoft Go Global](https://msdn.microsoft.com/goglobal).

## <a name="supported-programming-environments"></a>Environnements de programmation pris en charge

Vous pouvez ajouter une fonctionnalité MUI à une application de formulaires ou une application de console Win32 globalisée, comme décrit dans ce kit de développement logiciel (SDK). En outre, vous pouvez créer des applications gérées à l’aide de .NET Framework, qui est compatible avec MUI. Pour plus d’informations, consultez [développement .net](/previous-versions/ff361664(v=vs.100)).

## <a name="user-interface-language-settings"></a>Paramètres de langue de l’interface utilisateur

Lors de la planification de votre application MUI, vous devez d’abord déterminer les langues de l’interface utilisateur et la façon de les présenter à l’utilisateur. L’application peut prendre en charge les langues de l’une des manières suivantes :

-   Suivez les paramètres de langue du système. Supposons que les langues d’interface utilisateur préférées de l’utilisateur et les langues d’interface utilisateur préférées du système, prises ensemble, représentent les langues disponibles pour l’utilisateur. Utilisez le mécanisme de secours du chargeur de ressources pour la sélection de la langue.
-   Définissez les paramètres de langage spécifiques à l’application. Prenez en charge des langues spécifiques et présentez un mécanisme de sélection à l’utilisateur.

## <a name="resource-creation"></a>Création de ressources

Cette section décrit les possibilités de création des ressources de langue de l’interface utilisateur pour l’application. Pour plus d’informations, consultez [préparation des ressources](preparing-resources.md).

> [!Note]  
> Sur les systèmes d’exploitation antérieurs à Windows Vista, vous créez généralement des applications localisées en une seule langue, statiques et séparément, avec les langues prises en charge par les sections de ressources incluses dans les fichiers exécutables. Ce type d’implémentation est largement obsolète, et il est recommandé de choisir l’une des autres techniques de création de ressources décrites dans cette section, prises en charge pour Windows Vista et versions ultérieures. L’application peut ensuite être exécutée sur des systèmes d’exploitation antérieurs à Windows Vista à l’aide de [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya).

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a>Utilisation d’une seule langue dans une DLL de ressource (technologie de ressources MUI)

Une implémentation de ressource de DLL satellite standard est utilisée par de nombreuses applications Microsoft. Dans ce cas, un fichier exécutable principal est utilisé pour l’application MUI et une DLL de ressource est créée pour chaque langue prise en charge. L’utilisation d’une DLL satellite s’applique aux applications qui s’exécutent sur n’importe quel système d’exploitation Windows. Comme décrit dans [gestion des ressources MUI](mui-resource-management.md), la technologie de ressources MUI prend en charge une variante de l’implémentation de DLL satellite standard.

### <a name="use-of-multiple-languages-in-a-resource-dll"></a>Utilisation de plusieurs langues dans une DLL de ressource

Vous pouvez choisir de créer un fichier exécutable principal pour votre application MUI et une DLL de ressource pour les ressources associées aux langues prises en charge. Les copies du même identificateur de ressource sont définies dans le fichier de ressources de la langue de base (extension. RC) sous différentes balises de langue pour toutes les langues prises en charge.

### <a name="use-of-an-application-specific-resource-mechanism"></a>Utilisation d’un mécanisme de ressource Application-Specific

Vous pouvez planifier votre application MUI pour utiliser un mécanisme de ressource personnalisé. Dans ce cas, l’application gère le chargement des ressources de manière spécialisée.

## <a name="resource-localization"></a>Localisation des ressources

Pour prendre en charge les langues de l’interface utilisateur de votre application MUI, vous devez disposer des ressources linguistiques localisées. MUI prend en charge deux types de localisation, comme décrit dans le tableau suivant.



| Type de localisation       | Description                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Localisation pré-build  | Demandez la localisation avant de générer l’application et les ressources spécifiques à la langue. Le fichier de ressources de la langue de base pour les langues d’interface utilisateur prises en charge est copié et renommé pour chaque langue prise en charge, et les copies sont fournies aux localisateurs en fonction des besoins. |
| Localisation après génération | Demandez la localisation après avoir généré le fichier exécutable et la DLL de ressource pour votre application. Dans ce cas, une copie de la DLL de ressource est fournie à chaque localisateur.                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’interface utilisateur multilingue](about-multilingual-user-interface.md)
</dt> </dl>

 

 

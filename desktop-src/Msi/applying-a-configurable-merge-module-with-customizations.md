---
description: Suivez les instructions générales relatives à l’application des modules de fusion décrits dans application de fusion modules.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Application d’un module de fusion configurable avec des personnalisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9c771493a7a8e854472d840ffc21358c9741d8b3a8ea9876251456b6badf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829199"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Application d’un module de fusion configurable avec des personnalisations

Suivez les instructions générales relatives à l’application des modules de fusion décrits dans [application de fusion modules](applying-merge-modules.md). En outre, les consommateurs de module de fusion doivent effectuer les opérations suivantes pour configurer un module de fusion au moment de l’installation :

-   Utilisez un module de fusion créé pour avoir des paramètres configurables. Pour plus d’informations, consultez [création d’un module de fusion qui peut être configuré par l’utilisateur final](creating-a-merge-module-that-can-be-configured-by-the-end-user.md) .
-   Utilisez un outil de fusion et de configuration qui appelle Mergemod.dll version 2,0 ou ultérieure. Les versions antérieures de Mergmod.dll ne peuvent pas configurer les paramètres de module de fusion. Les auteurs doivent créer des modules de fusion qui fournissent des valeurs par défaut et sont compatibles avec les versions antérieures de Mergmod.dll.
-   Fournissez des informations de personnalisation lorsque l’outil client de configuration vous y invite. Les auteurs doivent créer des modules de fusion qui utilisent des valeurs par défaut lorsqu’un utilisateur refuse de fournir des informations.

 

 




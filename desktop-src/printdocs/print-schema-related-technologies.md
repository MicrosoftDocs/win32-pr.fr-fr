---
description: Explorez les technologies liées au schéma d’impression. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: Imprimer des technologies Schema-Related
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2948108b8bd6f581608471c9646fe135f83cb91561dc3c4cca97ac4df10560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112269"
---
# <a name="print-schema-related-technologies"></a>Imprimer des technologies Schema-Related

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

pour la .NET Framework 3,0, Windows Vista et versions ultérieures, les technologies PrintCapabilities et PrintTicket étendent les fonctionnalités du schéma d’impression pour offrir une expérience d’impression plus riche.

## <a name="printcapabilities"></a>PrintCapabilities

La technologie PrintCapabilities est une méthode de publication des paramètres contrôlés par l’utilisateur Description des attributs et des paramètres par travail. PrintCapabilities sont publiés dans un document XML (eXtensible Markup Language) appelé document PrintCapabilities, composé de termes définis dans les mots clés du schéma d’impression et les extensions privées. Le document PrintCapabilities peut être considéré comme un « instantané » de l’État configurable par l’utilisateur Configuration de l’appareil actuel, ainsi qu’une description des configurations possibles. Les appareils (ou pilotes de périphérique) génèrent un document PrintCapabilities (l’instantané) de leur ensemble actuel d’options configurables lorsqu’ils sont interrogés par des clients, qui peuvent être des applications ou le sous-système d’impression. Ce document décrit tous les PrintCapabilities configurables actuellement disponibles sur l’appareil, tels que les options de finition et les options de mise en page. Le document PrintCapabilities décrit explicitement tous les attributs de l’appareil et les paramètres autorisés pour chaque attribut. À l’aide de l’infrastructure du schéma d’impression, les attributs de l’appareil peuvent être décrits avec précision et comparés efficacement. En utilisant les mots clés contenus dans le document des mots clés du schéma d’impression et la structure définie dans l’infrastructure du schéma d’impression, les appareils peuvent permettre aux clients d’utiliser plus efficacement PrintCapabilities. Pour plus d’informations, consultez [schéma PrintCapabilities et construction de document](printcapabilities-schema-and-document-construction.md).

par rapport au sous-système d’impression de Microsoft Windows Server 2003 et versions antérieures, la technologie PrintCapabilities permet aux composants client et sous-système d’impression d’afficher de manière transparente les informations contenues dans le fichier binaire du système Win32 PrintCapabilities actuel. Cela permet au client d’interroger PrintCapabilities, de recevoir un instantané XML cohérent et bien compris, et de l’utiliser pour construire un PrintTicket pour un appareil sans appeler l’interface utilisateur (IU) du pilote.

## <a name="printticket"></a>PrintTicket

La technologie PrintTicket est le successeur de la structure DEVMODE actuelle. Il s’agit d’un document basé sur un langage de balisage eXtensible qui spécifie et conserve des informations sur la mise en forme et la configuration du travail d’impression. Une instance PrintTicket affecte des paramètres d’appareil particuliers et transmet l’intention de l’utilisateur. Il existe deux types de des PrintTicket : les des PrintTicket génériques, qui ne sont pas générés pour un appareil particulier ; et les des PrintTicket spécifiques à l’appareil, qui sont construits pour un appareil particulier. Les des PrintTicket génériques, qui sont destinés à être portables sur plusieurs appareils, dérivent leur contenu en sélectionnant des paramètres pour chacun des attributs d’appareil décrits exclusivement dans les mots clés du schéma d’impression. Les des PrintTicket spécifiques au périphérique dérivent leur contenu à partir d’un document PrintCapabilities, en sélectionnant les paramètres de chaque attribut d’appareil publié par ce document. Ces des PrintTicket peuvent également inclure des extensions privées, spécifiques à un modèle d’appareil ou à une famille de modèle d’appareil. Pour plus d’informations, consultez [schéma PrintTicket et construction de document](printticket-schema-and-document-construction.md).

Par rapport au sous-système d’impression actuel, la technologie PrintTicket permet à tous les composants et clients du sous-système d’impression d’avoir un accès transparent aux informations actuellement stockées dans les parties publiques et privées de la structure DEVMODE, à l’aide d’un format XML bien défini. Cette conception résout les problèmes actuels rencontrés dans les scénarios de mise à niveau de pilote ou de déclassement et de non-correspondance des pilotes dans les pilotes conçus pour la technologie PrintTicket. Ces scénarios peuvent entraîner une perte de paramètres et, par conséquent, une expérience client négative. Le PrintTicket active également de nouveaux scénarios, tels que l’activation d’un pilote d’imprimante pour exposer ses paramètres DEVMODE privés aux applications et aux plug-ins personnalisés de manière cohérente et non ambiguë. Cela permet d’augmenter la transparence des composants d’impression et de gérer les migrations de paramètres de manière plus propre. Les interfaces PrintTicket seront exposées aux applications via des méthodes sur des objets de code managé qui seront également disponibles pour les scripts. dans la nouvelle infrastructure d’application reposant sur des objets de code managé dans le .NET Framework 3,0, le PrintTicket est le moyen standard de décrire les paramètres de document.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




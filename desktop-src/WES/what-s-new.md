---
title: nouveautés (Windows journal des événements)
description: cette page récapitule les nouvelles fonctionnalités qui ont été ajoutées à l’API du journal des événements Windows pour chaque version.
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f80af15d6f8b6d95533fff296ee22ea3c82d2add5f21964a7863ac3d676f5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904119"
---
# <a name="whats-new-windows-event-log"></a>nouveautés (Windows journal des événements)

cette page récapitule les nouvelles fonctionnalités qui ont été ajoutées à l’API du journal des événements Windows pour chaque version.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 et Windows Server 2008 R2

Les modifications apportées au schéma [EventManifest](eventmanifestschema-schema.md) sont les suivantes :

-   Suppression du type complexe [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) . Pour fournir les mêmes fonctionnalités, utilisez des OpCodes spécifiques à la tâche (consultez l’élément **OpCodes** du type complexe [**TaskType**](eventmanifestschema-tasktype-complextype.md) .
-   Ajout des types simples [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md), [**filePath**](eventmanifestschema-filepath-simpletype.md)et [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) pour restreindre les valeurs affectées aux attributs de ces types.
-   Ajout de l’attribut **Filters** au type complexe [**ProviderType**](eventmanifestschema-providertype-complextype.md) . Les fournisseurs peuvent utiliser des filtres de la même façon que les fournisseurs utilisent le niveau et les mots clés pour déterminer s’ils doivent écrire un événement.
-   Ajout des types de sortie suivants que vous pouvez spécifier pour les éléments de données définis dans un modèle de données d’événement :
    -   Win : DateTimeCultureInsensitive
    -   Win : HResult
    -   Win : NTSTATUS
-   Les types de sortie sont maintenant honorés, alors qu’ils ne le sont pas.

les modifications suivantes ont été apportées à la version du [**compilateur de messages**](message-compiler--mc-exe-.md) fournie avec la version Windows 7 du SDK Windows :

-   Ajout d’arguments pour que le compilateur génère le code de journalisation en fonction de votre manifeste. vous pouvez également demander que le compilateur génère du code pour consigner les événements sur les systèmes d’exploitation antérieurs à Windows Vista. Pour obtenir la liste des arguments, consultez la section « arguments spécifiques à la génération du code utilisé pour journaliser les événements » de la rubrique [**du compilateur de message**](message-compiler--mc-exe-.md) .
-   Le compilateur applique désormais des validations syntaxiques et sémantiques plus strictes sur le manifeste. Cela peut entraîner l’utilisation de certains manifestes compilés avec succès sur les versions précédentes du compilateur de message pour que les modifications soient correctement compilées à l’aide de la version la plus récente.

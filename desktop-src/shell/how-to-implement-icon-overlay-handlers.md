---
description: Les gestionnaires de superposition d’icône sont des objets COM (Component Object Model) in-process, implémentés en tant que dll.
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: Comment implémenter des gestionnaires de superposition d’icône
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8745d0d5c0cf9c69f28f0235ecc82acb07a14f1e3408d7fa7d65cf729e01403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859696"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>Comment implémenter des gestionnaires de superposition d’icône

Les gestionnaires de superposition d’icône sont des objets COM (Component Object Model) in-process, implémentés en tant que dll. Ils exportent une interface en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellIconOverlayIdentifier**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier). Cette interface a trois méthodes : [**IShellIconOverlayIdentifier :: GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo), [**IShellIconOverlayIdentifier :: getPriority,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)et [**IShellIconOverlayIdentifier :: IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof).

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-getoverlayinfo"></a>Étape 1 : implémentation de GetOverlayInfo

La méthode [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) est d’abord appelée pendant l’initialisation. La méthode retourne le chemin d’accès qualifié complet du fichier qui contient l’image de superposition d’icône et son index de base zéro dans le fichier. L’interpréteur de commandes ajoute ensuite l’image à la liste d’images système. Les superpositions d’icône peuvent être contenues dans n’importe quel type de fichier standard, y compris .exe, .dll et. ico.

Une fois l’initialisation terminée, l’interpréteur de commandes appelle [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) lorsqu’il doit afficher la superposition d’icône du gestionnaire. La méthode doit retourner le même nom de fichier et le même index qu’au cours de l’initialisation. Bien que l’interpréteur de commandes utilise l’image mise en cache dans la liste d’images système au lieu de charger l’image à partir du fichier, une superposition d’icône est toujours identifiée par son nom de fichier et son index.

### <a name="step-2-implementing-getpriority"></a>Étape 2 : implémentation de getPriority,

La méthode [**getPriority,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) est appelée uniquement pendant l’initialisation. Elle attribue une valeur de priorité à la superposition d’icône du gestionnaire. La valeur peut être comprise entre zéro et 100, où 100 est la priorité la plus basse. L’objectif de cette valeur de priorité est d’aider l’interpréteur de commandes à résoudre le conflit qui se produit lorsque plusieurs superpositions d’icône sont spécifiées pour un seul objet. Le Shell utilise d’abord un ensemble interne de règles pour déterminer la superposition d’icône de priorité la plus élevée. Si ces règles ne résolvent pas le conflit, les valeurs affectées à l’icône se chevauchent par **getPriority,** déterminer la priorité.

La valeur de priorité définie par [**getPriority,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) n’est pas un moyen fiable de résoudre les conflits entre les gestionnaires de superposition d’icône sans relation. Il n’existe aucun moyen pour votre gestionnaire de déterminer les valeurs de priorité que les autres gestionnaires utilisent. Normalement, vous devez définir la valeur sur zéro. Toutefois, la valeur de priorité est utile lorsque vous avez implémenté deux ou plusieurs gestionnaires de superposition d’icône qui peuvent demander des icônes de superposition d’icône pour le même objet. En définissant les valeurs de priorité de manière appropriée, vous pouvez spécifier les superpositions d’icône requises qui seront affichées.

### <a name="step-3-implementing-ismemberof"></a>Étape 3 : implémentation de IsMemberOf

L’interpréteur de commandes appelle la méthode [**IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) pour déterminer s’il doit afficher la superposition d’icône d’un gestionnaire pour un objet particulier. L’interpréteur de commandes spécifie l’objet en passant son nom à la méthode. Si un gestionnaire souhaite afficher la superposition de son icône, **IsMemberOf** retourne la valeur S \_ OK. Si ce n’est pas le cas, elle retourne S \_ false.

Les gestionnaires de superposition d’icône sont normalement conçus pour fonctionner avec un groupe de fichiers particulier. Un [type de fichier](fa-file-types.md), identifié par une extension de nom de fichier spécifique, en est un exemple classique. Un gestionnaire de superposition d’icône peut demander une superposition d’icône pour tous les fichiers du type de fichier. Certains gestionnaires demandent une superposition d’icône uniquement si un fichier du type de fichier est dans un état particulier. Toutefois, les gestionnaires de superposition d’icône sont libres de demander leur superposition d’icône pour tout objet qu’ils choisissent.

 

 

---
title: Faire glisser les responsabilités source
description: Faire glisser les responsabilités source
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106512530"
---
# <a name="drag-source-responsibilities"></a>Faire glisser les responsabilités source

La source de glissement est chargée des tâches suivantes :

-   Fournir un objet de transfert de données pour la cible de déplacement qui expose les interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .
-   Génération des commentaires du pointeur et de la source.
-   Détermination du moment où l’opération glisser a été annulée ou une opération de suppression s’est produite.
-   Effectuer une action sur les données d’origine provoquée par l’opération de déplacement, telle que la suppression des données ou la création d’un lien vers celui-ci.

La tâche principale consiste à créer un objet de transfert de données qui expose les interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) . La source de glissement peut ou non inclure une copie des données sélectionnées. L’inclusion n’est pas obligatoire, mais cela vous permet de vous protéger contre les modifications involontaires et permet au code des opérations du presse-papiers d’être identique au code de glisser-déplacer.

Pendant qu’une opération glisser est en cours, la source de glissement est chargée de définir le pointeur de la souris et, le cas échéant, de fournir des commentaires sources supplémentaires à l’utilisateur. La source de glissement ne peut pas fournir de commentaires qui suivent la position de la souris autrement qu’en définissant réellement le pointeur réel (consultez la fonction [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) ). Cette règle doit être appliquée pour éviter les conflits avec les commentaires fournis par la cible de déplacement. (Une source de glissement peut également être une cible de déplacement. En cas de suppression sur lui-même, la source/cible peut, bien sûr, fournir des commentaires ciblés pour suivre la position de la souris. Dans ce cas, toutefois, il s’agit de la cible de déplacement qui effectue le suivi de la souris, et non de la source.) En fonction des commentaires offerts par la cible de déplacement, la source définit un pointeur approprié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Glisser-déposer](drag-and-drop.md)
</dt> </dl>

 

 
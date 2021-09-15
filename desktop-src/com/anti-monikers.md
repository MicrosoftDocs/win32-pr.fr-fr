---
title: Anti-monikers
description: OLE fournit une implémentation d’un type spécial de moniker appelé anti-moniker.
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525001"
---
# <a name="anti-monikers"></a>Anti-monikers

OLE fournit une implémentation d’un type spécial de moniker appelé *anti-moniker*. Vous utilisez ce moniker dans la création de nouvelles classes de moniker. Vous l’utilisez comme inverse du moniker sur lequel il est composé, en annulant efficacement ce moniker, de la même façon que l’opérateur « .. » déplace un niveau de répertoire dans une commande de système de fichiers.

Il est nécessaire d’avoir un anti-moniker disponible, car une fois qu’un moniker composite est créé, il n’est pas possible de supprimer des parties du moniker si, par exemple, un objet est déplacé. Au lieu de cela, vous utilisez un anti-moniker pour supprimer une ou plusieurs entrées d’un moniker composite.

Les anti-monikers sont une classe de moniker explicitement conçue pour une utilisation en tant qu’inverse. COM définit la fonction [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) nommée, qui retourne un anti-moniker. Cette fonction est généralement utilisée pour implémenter la méthode [**IMoniker :: inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) .

Un anti-moniker est uniquement un inverse pour les types de monikers implémentés pour traiter les anti-monikers comme un inverse. Par exemple, si vous souhaitez supprimer la dernière partie d’un moniker composite, vous ne devez pas créer de anti-moniker et le composer à la fin du composite. Vous ne pouvez pas être sûr que la dernière pièce composite considère qu’un anti-moniker est son inverse. Au lieu de cela, vous devez appeler [**IMoniker :: enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) sur le moniker composite, en spécifiant **false** comme premier paramètre. Cela crée un énumérateur qui retourne les monikers de composant dans l’ordre inverse. Utilisez l’énumérateur pour récupérer la dernière pièce du composite et appelez l' [**inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) sur ce moniker. Le moniker retourné par **inverse** est ce dont vous avez besoin pour supprimer la dernière partie du composite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers composites](composite-monikers.md)
</dt> <dt>

[Monikers de fichiers](file-monikers.md)
</dt> <dt>

[Monikers d’élément](item-monikers.md)
</dt> <dt>

[Monikers de pointeur](pointer-monikers.md)
</dt> </dl>

 

 





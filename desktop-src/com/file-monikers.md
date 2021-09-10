---
title: Monikers de fichiers
description: Monikers de fichiers
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363364"
---
# <a name="file-monikers"></a>Monikers de fichiers

Les *monikers de fichiers* sont la classe moniker la plus simple. Les monikers de fichiers peuvent être utilisés pour identifier tout objet stocké dans son propre fichier. Un moniker de fichier agit comme un wrapper pour le nom de chemin d’accès que le système de fichiers natif affecte au fichier. L’appel de [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) pour ce moniker provoquerait l’activation de cet objet, puis retournerait un pointeur d’interface vers l’objet. La source de l’objet nommé par le moniker doit fournir une implémentation de l’interface [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) pour prendre en charge la liaison d’un moniker de fichier. Les monikers de fichiers peuvent représenter un chemin d’accès complet ou relatif.

Par exemple, le moniker de fichier pour un objet Spreadsheet stocké en tant que fichier C : \\ Work \\MySheet.xls contient des informations équivalentes à ce nom de chemin d’accès. Toutefois, le moniker ne se compose pas nécessairement de la même chaîne. La chaîne est simplement son *nom displayÂ*, une représentation du contenu du moniker qui est explicite pour un utilisateur final. Le nom complet, qui est disponible par le biais de la méthode [**IMoniker :: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) , est utilisé uniquement lors de l’affichage d’un moniker pour un utilisateur final. Cette méthode obtient le nom complet de l’une des classes de moniker. En interne, le moniker peut stocker les mêmes informations dans un format plus efficace pour effectuer des opérations de moniker, mais n’est pas significatif pour les utilisateurs. Ensuite, lorsque ce même objet est lié via un appel à la méthode [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , l’objet est activé, probablement en chargeant le fichier dans la feuille de calcul.

OLE offre aux fournisseurs de monikers la fonction d’assistance [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) qui crée un objet moniker de fichier et retourne son pointeur au fournisseur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Anti-monikers](anti-monikers.md)
</dt> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers composites](composite-monikers.md)
</dt> <dt>

[Monikers d’élément](item-monikers.md)
</dt> <dt>

[Monikers de pointeur](pointer-monikers.md)
</dt> </dl>

 

 





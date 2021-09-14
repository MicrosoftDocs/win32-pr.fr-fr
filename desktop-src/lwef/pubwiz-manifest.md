---
title: Utilisation du manifeste de transfert
description: L’Assistant Publication de sites Web et l’Assistant commande d’impression en ligne utilisent le manifeste de transfert pour communiquer les détails du transfert de données entre l’ordinateur client et le site serveur.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Assistant Publication de sites Web, manifeste de transfert
- Assistant commande d’impression en ligne, manifeste de transfert
- transférer le manifeste
- manifest
- Window. external, manifeste de transfert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118178"
---
# <a name="using-the-transfer-manifest"></a>Utilisation du manifeste de transfert

L’Assistant Publication de sites Web et l’Assistant commande d’impression en ligne utilisent le manifeste de transfert pour communiquer les détails du transfert de données entre l’ordinateur client et le site serveur.

## <a name="the-purpose-of-the-transfer-manifest"></a>Objectif du manifeste de transfert

Le manifeste de transfert décrit les fichiers impliqués dans le transfert, y compris les détails tels que la hiérarchie de destination et les métadonnées du fichier. Le script côté serveur peut modifier le manifeste en supprimant les fichiers inappropriés de la liste et en ajoutant des informations sur le mode et l’emplacement de transfert des fichiers.

Le manifeste est exposé en tant que propriété **Window. external. Property ("TransferManifest")**, Document XML Document Object Model (DOM). Pour plus d’informations sur le modèle DOM XML, consultez la documentation MSDN relative à [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).

L’organisation de niveau supérieur du manifeste de transfert est la suivante :


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



La page HTML côté serveur peut utiliser les nœuds du manifeste pour obtenir certaines informations sur les fichiers à copier, puis modifier l’interface utilisateur du service en conséquence. Par exemple, un site d’impression de photos peut utiliser les informations pour afficher des miniatures des images choisies, alors qu’un site de stockage peut utiliser ces informations pour s’assurer qu’un espace de stockage suffisant est disponible pour cet utilisateur. Pour obtenir des informations complètes sur les nœuds et les attributs du manifeste de transfert, consultez [transférer le schéma de manifeste](/windows/desktop/shell/interfaces).

Le schéma de manifeste de transfert est écrit sous la forme d’un modèle ouvert, de sorte que les éléments qui ne sont pas spécifiquement définis dans le schéma peuvent apparaître dans le manifeste de transfert. Par conséquent, un site de fournisseur peut ajouter des éléments propriétaires pour sa propre utilisation sans perturber la validité du manifeste. Le schéma est également défini de sorte que l’ordre des éléments ne soit pas limité.

> [!Note]  
> Le manifeste est recréé chaque fois qu’un nouveau fournisseur est choisi afin que le fournisseur puisse stocker les informations de site dans le manifeste.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de manifeste de transfert](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 
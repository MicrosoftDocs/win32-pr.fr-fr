---
title: Énumération des objets conteneurs
description: Par Convention, tous les éléments d’une énumération dans ADSI doivent être du même type de données Automation. Par exemple, une énumération ne doit pas retourner certains éléments sous la forme d’une variante de type VT \_ I4 et d’autres en tant que variante de type VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff6bb6d05a34ce6434531338a877d2dd4aaee2cd4df0b38c81b50b7f56db4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428558"
---
# <a name="enumerating-container-objects"></a>Énumération des objets conteneurs

Par Convention, tous les éléments d’une énumération dans ADSI doivent être du même type de données Automation. Par exemple, une énumération ne doit pas retourner certains éléments sous la forme d’une **variante** de type **VT \_ I4** et d’autres en tant que **variante** de type **VT \_ BSTR**.

Pour énumérer une liste d’éléments gérés par un objet, un client demande la création d’un objet d’énumération pour le type spécifique d’informations qui sont répertoriées. Dans ADSI, le client peut répertorier les objets dans les objets d’espace de noms, les objets conteneurs génériques, les objets de collection, les objets membres ou les objets de schéma. L’interface ADSI fournit un filtre qui peut être défini et modifié pour limiter les correspondances dans toute énumération par le biais de la propriété [**IADsContainer. Filter**](iadscontainer-property-methods.md) . Des exemples d’implémentations d’objets Enumerator se trouvent dans l’exemple de code du composant fournisseur pour les objets conteneur ADs suivants.



| Type d’objet         | code         |
|---------------------|--------------|
| Conteneur générique   | cenumobj. cpp |
| Conteneur d’espace de noms | cenumns. cpp  |
| Conteneur de schéma    | cenumsch. cpp |



 

Pour plus d’informations côté client, consultez [collections et groupes](collections-and-groups.md).

 

 





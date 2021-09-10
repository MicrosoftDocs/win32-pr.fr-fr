---
title: Clé ProgID
description: Un identificateur programmatique (ProgID) est une entrée de Registre qui peut être associée à un CLSID. À l’instar du CLSID, le ProgID identifie une classe mais avec moins de précision, car il n’est pas garanti qu’il soit globalement unique.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363347"
---
# <a name="progid-key"></a>Clé ProgID

Un identificateur programmatique (ProgID) est une entrée de Registre qui peut être associée à un CLSID. À l’instar du CLSID, le ProgID identifie une classe mais avec moins de précision, car il n’est pas garanti qu’il soit globalement unique.

## <a name="registry-entry"></a>Entrée de Registre

**HKEY \_ \_ \\ \\ Classes logicielles de l’ordinateur local** \\ *{* ProgID *}*



| Clé de Registre                            | Description                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [**IDENTIFICATEUR**](clsid.md)                  | Associe un ProgID à un CLSID.                                  |
| [**Insertable**](insertable-progid.md) | Indique que cette classe peut être insérée dans des conteneurs OLE 2.       |
| [**Protocol**](protocol.md)            | Indique que cette classe OLE 2 peut être insérée dans les conteneurs OLE 1. |
| [**Shell**](shell.md)                  | fournit les informations d’impression et d' **ouverture de fichier** Windows 3,1. |



 

## <a name="remarks"></a>Remarques

Vous pouvez utiliser un ProgID dans des situations de programmation où il n’est pas possible d’utiliser un CLSID. Les ProgID ne doivent pas apparaître dans l’interface utilisateur. Il n’est pas garanti que les ProgID soient uniques, donc ils ne peuvent être utilisés que lorsque des collisions de noms sont gérables.

Le format d’un ProgID est <*programme*>. <*composant*>. <*version* , séparé par des points et sans espaces, comme dans> ument. 6. Le ProgID doit respecter les exigences suivantes :

-   Ne pas comporter plus de 39 caractères.
-   Ne pas contenir de signes de ponctuation (y compris les traits de soulignement), à l’exception d’un ou plusieurs points.
-   Ne commence pas par un chiffre.
-   Être différent du nom de classe d’une application OLE 1, y compris la version OLE 1 de la même application, le cas échéant.

Étant donné que le ProgID ne doit pas apparaître dans l’interface utilisateur, vous pouvez obtenir un nom affichable en appelant [**IOleObject :: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype). Consultez également [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).

La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IOleObject :: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 





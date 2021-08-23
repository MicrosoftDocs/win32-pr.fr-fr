---
title: Clé ProgID indépendante de la version
description: Associe un ProgID à un CLSID. Cette clé est utilisée pour déterminer la dernière version d’une application d’objet.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dec371f87ff3aba98bd642537e4de893df20682cc9bd84eda8829f24d241b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567969"
---
# <a name="version-independent-progid-key"></a>Clé ProgID indépendante de la version

Associe un ProgID à un CLSID. Cette clé est utilisée pour déterminer la dernière version d’une application d’objet.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Remarques

La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.

Le format pour <*ProgID indépendant* de la version> est <*programme*>. <*composant*>, séparé par des points, sans espace et sans numéro de version. Le ProgID indépendant de la version, comme le ProgID, peut être inscrit avec un nom explicite.

*ProgID* est le ProgID de la dernière version installée de la classe.

Les applications doivent inscrire un identificateur de programmation indépendant de la version sous la clé *ProgID indépendante* de la version. le ProgID indépendant de la version fait référence à la classe de l’application et ne passe pas de la version à la version, et non à la constante restante dans tous les versionsâ, par exemple, Microsoft Word Document. Il est utilisé avec les langages de macro et fait référence à la version actuellement installée de la classe de l’application. Le ProgID indépendant de la version doit correspondre au nom de la version la plus récente de l’application objet.

Par exemple, le ProgID indépendant de la version est utilisé lorsqu’une application conteneur crée un graphique ou une table avec un bouton de barre d’outils. Dans ce cas, l’application peut utiliser le ProgID indépendant de la version pour déterminer la version la plus récente de l’application objet nécessaire.

Le ProgID indépendant de la version est stocké et géré uniquement par le code d’application. Lorsqu’il reçoit le ProgID indépendant de la version, la fonction [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retourne le CLSID de la version actuelle.

Vous pouvez utiliser [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) et [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) pour effectuer une conversion entre ces deux représentations.

Vous pouvez utiliser [**IOleObject :: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) ou [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) pour remplacer l’identificateur par une chaîne affichable.

Si un gestionnaire personnalisé n’est pas utilisé, l’entrée doit être définie sur OLE32.DLL, comme illustré dans l’exemple suivant :

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<ProgID> Essentiel](-progid--key.md)
</dt> </dl>

 

 





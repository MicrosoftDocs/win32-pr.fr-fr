---
title: Clé FileType
description: Utilisé par GetClassFile pour faire correspondre des modèles à différents octets de fichier dans un fichier non composé.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Clé de Registre FileType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923240"
---
# <a name="filetype-key"></a>Clé FileType

Utilisé par [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) pour faire correspondre des modèles à différents octets de fichier dans un fichier non composé.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span id="offset"></span><span id="OFFSET"></span>*décalage*
</dt> <dd>

Détermine la distance à partir du début ou de la fin du fichier pour commencer la comparaison. Si le décalage est une valeur négative, la comparaison commence à la fin du fichier moins la valeur de décalage. La valeur de décalage est un type décimal, sauf si elle est précédée de « 0x ».

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*libéré*
</dt> <dd>

Représente la longueur en octets entre le début et la fin du fichier. Représente la plage d’octets dans le fichier. La valeur *CB* est une valeur décimale, sauf si elle est précédée de « 0x ».

</dd> <dt>

<span id="mask"></span><span id="MASK"></span>*filtrage*
</dt> <dd>

Valeur binaire utilisée pour le masquage, qui est effectuée à l’aide d’une opération AND logique, et la plage d’octets spécifiée par *offset* et *CB*. Si cette valeur est omise, les octets sont définis sur tous. Cette valeur est toujours hexadécimale.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*ajoutée*
</dt> <dd>

Représente le modèle qui doit correspondre pour qu’un fichier soit de ce type de fichier. Le modèle est utilisé pour identifier correctement un format de fichier connu à partir de son contenu, et non par son extension.

</dd> </dl>

## <a name="remarks"></a>Notes

Les entrées sont utilisées par la fonction [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) pour faire correspondre des modèles à différents octets de fichier dans un fichier non composé. **Filetype** contient des sous-clés CLSID, chacune ayant une série de sous-clés **0**, **1**, **2**, **3**. Ces valeurs contiennent des modèles qui, si une correspondance est trouvée, génèrent le CLSID indiqué. Par exemple, la valeur « 0, 4, FFFFFFFF, ABCD1234 » indique que les 4 premiers octets doivent être ABCD1234, dans cet ordre. La valeur « -4, 4, FEFEFEFE » indique que les quatre derniers octets du fichier doivent être FEFEFEFE. Si l’un des modèles correspond, le CLSID est retourné.

La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extension de fichier<\_>**](-file-extension--key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 





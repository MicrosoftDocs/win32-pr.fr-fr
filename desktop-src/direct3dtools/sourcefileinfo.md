---
description: Représente des informations sur un fichier de code source.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SourceFileInfo, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481992"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo, structure

Représente des informations sur un fichier de code source.

## <a name="syntax"></a>Syntaxe


```C++
} SourceFileInfo;
```

## <a name="members"></a>Membres

**fileName**  
Chaîne COM comtaining le chemin d’accès du fichier source associé.

**checksumByteCount**  
Nombre d’octets dans la somme de contrôle. Lorsque checkSumAlgorithm est égal à CHECKSUMALGORITHM :: MD5, checkSumByteCount est 16. Lorsque checkSumAlgorithm est égal à CHECKSUMALGORITHM :: SHA1, checkSumByteCount est 20.

**checkSumAlgorithm**  
Spécifie l’algorithme utilisé pour générer la somme de contrôle du fichier. Les algorithmes pris en charge sont MD5 et SHA1. Pour plus d’informations, consultez l’énumération CHECKSUMALGORITHM.

**checkSumFirstPart**  
Première partie de 8 octets de la somme de contrôle.

**checkSumSecondPart**  
Deuxième partie de 8 octets de la somme de contrôle.

**checkSumThirdPart**  
Troisième partie de 8 octets de la somme de contrôle.

**checkSumFourthPart**  
Quatrième partie de 8 octets de la somme de contrôle.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 




---
title: commutateur/savePP
description: Quand la directive/savePP est spécifiée, le compilateur MIDL ne supprime pas la sortie du préprocesseur C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- MIDL du commutateur/savePP
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030255"
---
# <a name="savepp-switch"></a>commutateur/savePP

Quand la directive **/savePP** est spécifiée, le compilateur MIDL ne supprime pas la sortie du préprocesseur C/C++.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Ce commutateur permet aux développeurs de discerner ce qui est analysé par le compilateur MIDL et est utile pour le débogage. La sortie du préprocesseur est écrite dans un ou plusieurs fichiers temporaires dans le répertoire indiqué par la variable d’environnement TEMP. Le nom du fichier de sortie, ou fichiers, suit une convention d’affectation de noms de MID \* . tmp. Notez qu’une seule compilation peut générer plusieurs flux d’entrée prétraités ; Cela est dû au fait que l’importation d’un fichier IDL, par opposition à l’utilisation de **\# include**, entraîne une exécution de préprocesseur distincte.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/CPP \_ opt**](-cpp-opt.md)
</dt> <dt>

[/non \_ CPP,/nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 





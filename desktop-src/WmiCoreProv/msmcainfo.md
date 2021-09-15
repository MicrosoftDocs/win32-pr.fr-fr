---
description: Classe de base abstraite à partir de laquelle toutes les classes de données du fournisseur MCA (machine Check architecture), telles que MSMCAInfo \_ RawMCAData, sont dérivées. cette classe est disponible uniquement dans les systèmes Windowss 64 bits.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: MSMCAInfo, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518952"
---
# <a name="msmcainfo-class"></a>MSMCAInfo, classe

La classe **MSMCAInfo** est une classe de base abstraite à partir de laquelle toutes les classes de données du fournisseur MCA (machine Check architecture), telles que [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md), sont dérivées. Le fournisseur MCA possède également des classes d’événements, dérivées de [**WmiEvent**](wmievent.md). cette classe est disponible uniquement dans les systèmes Windowss 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Membres

La classe **MSMCAInfo** ne définit aucun membre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                         |
| Espace de noms<br/>                | \\WMI racine<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes MSMCA](msmca-classes.md)
</dt> <dt>

[**\_En-tête MSMCAEvent**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 





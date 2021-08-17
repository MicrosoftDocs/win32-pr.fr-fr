---
title: Constantes d’énumération (WSManDisp. h)
description: L’énumération contient des constantes, telles qu’elles sont répertoriées dans la liste suivante, utilisées dans le paramètre flags par des appels à l’énumération de session. Enumerate et IWSManSession.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c8182352d2ebf3763a38f74dd6f100dc836e88cfa10212ffaa971048ebd1aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113261"
---
# <a name="enumeration-constants"></a>Constantes d’énumération

L’énumération **\_ \_ WSManEnumFlags** contient des constantes, telles qu’elles sont répertoriées dans la liste suivante, utilisées dans le paramètre *Flags* par des appels à [**session. Enumerate**](session-enumerate.md) et [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

Sachez que **WSManFlagReturnObject** et **WSManFlagHierarchyDeep** sont la valeur par défaut si le paramètre *Flags* n’est pas spécifié.

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Les lots contiennent les instances XML demandées. Il s’agit de la valeur par défaut pour le paramètre flag.

La méthode de script associée est [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) et la méthode C++ est [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Cet indicateur contrôle la manière dont le paramètre de *filtre* dans l’appel à [**session. Enumerate**](session-enumerate.md) est interprété par WinRM.

Le format du filtre peut être un fragment XML ou une chaîne de texte brut. Le format est déterminé par le [*dialecte de filtre*](windows-remote-management-glossary.md) du [*filtre*](windows-remote-management-glossary.md) utilisé dans l’appel à [**session. Enumerate**](session-enumerate.md) ou [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), qui est spécifique à l’opération effectuée.

Si le paramètre de *dialecte* n’est pas spécifié, WinRM tente de déterminer le dialecte en fonction du premier caractère du filtre. Si le premier caractère est <, mais que le filtre n’est pas en fait un fragment XML, cet indicateur doit être défini. Par exemple, un filtre au format suivant nécessite que vous dédéfinissez **WSManFlagNonXmlText** pour que le filtre soit correctement interprété :

`<25 && > 1`

Si le filtre est un fragment XML, cet indicateur n’est pas nécessaire, car le fragment commence par <, que WinRM interprète correctement comme XML. Par exemple,

`<filter>select * from aDataStructure</filter>`

Si le filtre est en texte brut qui ne commence pas par <, cet indicateur n’est pas obligatoire. Par exemple,

`select * from aDataStructure`

La méthode de script associée est [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) et la méthode C++ est [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Les lots contiennent des références de point de terminaison (ERP) pour les instances XML correspondantes, mais pas les instances réelles.

La méthode de script associée est [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) et la méthode C++ est [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Les lots contiennent à la fois les instances XML demandées et les ERP correspondants contenus dans un élément [*WSMan : items*](windows-remote-management-glossary.md) .

La méthode de script associée est [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) et la méthode C++ est [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Les instances de classe dérivée sont incluses et sont représentées en fonction de leurs schémas réels.

La méthode de script associée est [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) et la méthode C++ est [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Les instances de classes dérivées sont exclues. Seules les instances du type demandé sont affichées.

La méthode de script associée est [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) et la méthode C++ est [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Les instances de classe dérivée sont incluses et sont représentées en fonction du schéma de la classe de base. Les propriétés définies dans la classe dérivée ne sont pas affichées.

La méthode de script associée est [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) et la méthode C++ est [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes et énumérations WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[Énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Interrogation d’instances spécifiques d’une ressource](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 






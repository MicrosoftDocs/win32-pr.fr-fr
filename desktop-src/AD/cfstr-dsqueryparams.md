---
title: CFSTR_DSQUERYPARAMS (DSQuery. h)
description: Le \_ format de presse-papiers CFSTR DSQUERYPARAMS fournit un handle de mémoire globale (HGLOBAL) qui contient une structure DSQUERYPARAMS.
ms.assetid: bb8aea98-8309-42bf-993d-fa408bb4deb2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSQUERYPARAMS
api_location:
- DSQuery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a330d228778f34118d232b2004e7294ab493ed77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941966"
---
# <a name="cfstr_dsqueryparams"></a>CFSTR \_ DSQUERYPARAMS

<dl> <dt>

<span id="CFSTR_DSQUERYPARAMS"></span><span id="cfstr_dsqueryparams"></span>**CFSTR \_ DSQUERYPARAMS**
</dt> <dd> <dl> <dt>

"DsQueryParameters"
</dt> <dt>



Le format de presse-papiers **CFSTR \_ DSQUERYPARAMS** est pris en charge par l' [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) fourni par la méthode [**ICommonQuery :: OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) . Le format de presse-papiers **CFSTR \_ DSQUERYPARAMS** fournit un handle de mémoire globale (**HGLOBAL**) qui contient une structure [**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>DSQuery. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> </dl>

 


---
description: la classe WBEMTime facilite les conversions entre les différentes Windows et les formats d’heure d’exécution C ANSI. Pour plus d’informations, consultez également méthodes de la classe WBEMTimeSpan.
ms.assetid: b633bc8c-9d02-4bcf-8528-10773fb5ae7a
ms.tgt_platform: multiple
title: WBEMTime, classe (WbemTime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEMTime
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 5d2f06b06db998dc18a876e0e5534e1d86c6ae89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918692"
---
# <a name="wbemtime-class"></a>WBEMTime, classe

\[La classe **WBEMTime** fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

la classe **WBEMTime** facilite les conversions entre les différentes Windows et les formats d’heure d’exécution C ANSI. Pour plus d’informations, consultez également méthodes de la [**classe WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Membres

La classe **WBEMTime** possède les types de membres suivants :

-   [Constructeurs](#constructors)
-   [Méthodes](#methods)

### <a name="constructors"></a>Constructeurs

La classe **WBEMTime** contient ces constructeurs.



| Constructeur                           | Description                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | constructeur qui facilite les conversions entre les différents Windows et les formats d’heure d’exécution C ANSI.<br/> |



 

### <a name="methods"></a>Méthodes

La classe **WBEMTime** possède ces méthodes.



| Méthode                                                           | Description                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Effacé**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Définit l’heure de l’objet **WBEMTime** sur une heure non valide.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Affiche l’heure sous la forme d’une valeur **BSTR** .<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Obtient l’heure sous la forme d’une valeur **BSTR** au format DateTime CIM.<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Obtient une date DMTF basée sur une FAT ou un format de [date et d’heure](date-and-time-format.md) où l’heure UTC n’est pas connue.<br/> |
| [**GetFILETIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Obtient l’heure sous la forme d’une structure **fileTime** MFC.<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Surchargé. Retourne le décalage en minutes (+ ou-) entre l’heure GMT et l’heure locale pour l’heure fournie dans l’argument.<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Obtient l’heure sous la forme d’une structure de **struct TM** Runtime C ANSI.<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Obtient l’heure sous la forme d’une structure **SystemTime** MFC.<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Obtient l’heure sous la forme d’un entier 64 bits.<br/>                                                                                          |
| [**GetTime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Obtient l’heure sous la forme d’une variable de temps t Runtime C ANSI \_ .<br/>                                                                       |
| [**IsOk**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Indique si l’objet **WBEMTime** représente une heure valide.<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Définit l’heure dans l’objet **WBEMTime** au format DateTime CIM.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>WBEMTime, opérateurs surchargés

L’objet **WBEMTime** définit les opérateurs surchargés suivants.



| WBEMTime, opérateurs surchargés                                                                                                                                                                                                                                                                                                                                                                                                                                        | Description                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**opérateur =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | l’opérateur d' *assignation* facilite les conversions entre différents Windows et les formats d’heure d’exécution C ANSI.                           |
| [**opérateur +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | L’opérateur d' *addition* incrémente l’heure d’un objet d’un intervalle de temps. Le résultat est retourné dans un nouvel objet **WBEMTime** .              |
| [**opérateur + =**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | L’opérateur *Add-and-Assign* incrémente l’heure d’un objet d’un intervalle de temps.                                                             |
| [**and**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | L’opérateur de *soustraction* décrémente l’heure d’un objet d’un autre objet. Le résultat est retourné dans un nouvel objet **WBEMTime** . |
| [**opérateur =**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | L’opérateur de *soustraction et d’assignation* décrémente l’heure d’un objet d’un intervalle de temps.                                                        |
| [**opérateur = =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to),[**opérateur ! =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**>d’opérateur**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**>opérateur =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**<d’opérateur**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**<opérateur =**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Les opérateurs de comparaison comparent deux objets **WBEMTime** .                                                                            |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



 


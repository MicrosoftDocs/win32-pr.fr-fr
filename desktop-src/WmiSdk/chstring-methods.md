---
description: La classe CHString expose les méthodes suivantes.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Méthodes CHString
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d15726702177aa484a070cca3ec1aab56d708b57991d3ff6a7aae43b1ccf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556954"
---
# <a name="chstring-methods"></a>Méthodes CHString

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

La classe [**CHString**](chstring.md) expose les méthodes suivantes.

## <a name="in-this-section"></a>Dans cette section

-   [**Méthode AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**Constructeurs CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**COLLATE, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare (méthode)**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**Méthode CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Empty, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Méthodes Find**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**Méthode FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**Méthodes de format**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**Méthodes FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**Méthode FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**Méthode FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**Méthode GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**GetAt, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer (méthode)**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**Méthode GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**GetData, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**GetLength, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty (méthode)**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Left, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**Méthode LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**Méthode LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**Méthode MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**Méthode MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**Méthode MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Méthodes Mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**Method, opérateur \[ \]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**CHString :: Operator +**](chstring--operator-plus.md)
-   [**CHString :: Operator + =**](chstring--operator-plus-equal.md)
-   [**CHString :: Operator =**](chstring--operator-equal.md)
-   [**Operator = = (constCHString&, constCHString&), méthode**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**Operator = = (constCHString&, constLPCWSTR&), méthode**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**méthode> Operator (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**méthode> Operator (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**Méthode Operator>= (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**Méthode Operator>= (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**méthode< Operator (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**méthode< Operator (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**Méthode Operator<= (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**Méthode Operator<= (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**Méthode Operator ! = (constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**Méthode Operator ! = (constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**Operator LPCWSTR, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**Méthode ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**Méthode ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Right, méthode**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**Méthode SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**Méthode SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**Méthode SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**Méthode TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**Méthode TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**Méthode UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 

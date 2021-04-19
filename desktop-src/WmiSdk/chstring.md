---
description: Le tableau suivant répertorie les méthodes CHString.
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.tgt_platform: multiple
title: CHString, classe (ChString. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CHString
- ??1CHString@@QAE@XZ
- ??1CHString@@QEAA@XZ
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 0c94fcd89a41e610d039afe17f4b56e58cb117bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532149"
---
# <a name="chstring-class"></a>CHString, classe

\[La classe **CHString** fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

Le tableau suivant répertorie les méthodes **CHString** .

## <a name="members"></a>Membres

La classe **CHString** possède les types de membres suivants :

-   [Constructeurs](#constructors)
-   [Méthodes](#methods)
-   [Opérateurs](#operators)

### <a name="constructors"></a>Constructeurs

La classe **CHString** contient ces constructeurs.



| Constructeur                           | Description                                                 |
|:--------------------------------------|:------------------------------------------------------------|
| [**CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_)) | Construit des chaînes **CHString** de différentes façons.<br/> |



 

### <a name="methods"></a>Méthodes

La classe **CHString** possède ces méthodes.



| Méthode                                                    | Description                                                                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)         | Alloue un BSTR à partir de données **CHString** .<br/>                                                            |
| [**COLLATE**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)                       | Compare deux chaînes (respecte la casse ; utilise des informations spécifiques aux paramètres régionaux).<br/>                            |
| [**Comparer**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)                       | Compare deux chaînes (respect de la casse).<br/>                                                              |
| [**CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)           | Compare deux chaînes (non-respect de la casse).<br/>                                                            |
| [**Vidé**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)                           | Force une chaîne à avoir une longueur égale à 0 (zéro).<br/>                                                            |
| [**Trouver**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))                        | Surchargé. Recherche un caractère ou une sous-chaîne à l’intérieur d’une chaîne plus grande.<br/>                                  |
| [**FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)                   | Recherche le premier caractère correspondant dans un ensemble.<br/>                                                      |
| [**Format**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))                         | Surchargé. Met en forme la chaîne en tant que **sprintf** .<br/>                                                 |
| [**FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))         | Surchargé. Met en forme une chaîne de message.<br/>                                                               |
| [**FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)                       | Met en forme la chaîne en tant que **vsprintf** .<br/>                                                            |
| [**FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)                   | Supprime toute surcharge de cette chaîne en libérant de la mémoire supplémentaire précédemment allouée à la chaîne.<br/> |
| [**GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)         | Retourne la taille de la mémoire tampon de chaîne.<br/>                                                              |
| [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))                           | Surchargé. Retourne le caractère à une position donnée.<br/>                                              |
| [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)                   | Retourne un pointeur vers les caractères de la chaîne **CHString** .<br/>                                     |
| [**GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength) | Retourne un pointeur vers les caractères de la chaîne **CHString** , en tronquant la longueur spécifiée.<br/> |
| [**GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)                       | Retourne un pointeur vers les données de la chaîne **CHString** .<br/>                                           |
| [**GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)                   | Retourne le nombre de caractères Unicode dans une chaîne **CHString** .<br/>                                  |
| [**IsEmpty**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)                       | Teste si une chaîne **CHString** ne contient aucun caractère.<br/>                                         |
| [**Gauche**](/windows/desktop/api/ChString/nf-chstring-chstring-left)                             | Extrait la partie gauche d’une chaîne (par exemple, la fonction **Left $** de base).<br/>                             |
| [**LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))               | Charge une chaîne **CHString** existante à partir d’un fichier de ressources.<br/>                                         |
| [**LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)                 | Désactive le décompte de références et protège la chaîne dans la mémoire tampon.<br/>                                  |
| [**MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)                   | Convertit tous les caractères de cette chaîne en caractères minuscules.<br/>                              |
| [**MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)               | Inverse les caractères de cette chaîne.<br/>                                                             |
| [**MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)                   | Convertit tous les caractères de cette chaîne en caractères majuscules.<br/>                              |
| [**ExtracChaîne**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))                               | Surchargé. Extrait la partie centrale d’une chaîne (telle que la fonction **Mid $** de base).<br/>                |
| [**ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)           | Libère le contrôle de la mémoire tampon retournée par [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer).<br/>                 |
| [**ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)               | Recherche un caractère dans une chaîne plus grande ; démarre à partir de la fin.<br/>                                      |
| [**Oui**](/windows/desktop/api/ChString/nf-chstring-chstring-right)                           | Extrait la partie droite d’une chaîne (par exemple, la fonction $ de base **Right** ).<br/>                           |
| [**SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)                           | Définit un caractère à une position donnée.<br/>                                                               |
| [**SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)           | Extrait une sous-chaîne qui contient uniquement les caractères qui ne sont pas dans le jeu.<br/>                     |
| [**SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)           | Extrait une sous-chaîne qui contient uniquement les caractères d’un jeu.<br/>                                    |
| [**TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)                     | Supprime les caractères d’espace blanc de début de la chaîne.<br/>                                                |
| [**TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)                   | Supprime les caractères d’espace blanc de fin de la chaîne.<br/>                                               |
| [**UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)             | Active le décompte de références et libère la chaîne dans la mémoire tampon.<br/>                                   |



 

### <a name="operators"></a>Opérateurs
`
The **CHString** class has these operators.`



| Opérateur                                                                                            | Description                                                                                                       |
|:----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| [**opérateur ! = (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))            | Compare deux **CHStrings** d’inégalité.<br/>                                                             |
| [**opérateur ! = (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))              | Compare un **CHString** avec un **LPCWSTR** pour vérifier l’inégalité.<br/>                                             |
| [**and \[\]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))                                                | Retourne le caractère à une substitution d’opérateur de position donnée pour [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int)).<br/> |
| [**opérateur +**](chstring--operator-plus.md)                                                       | Concatène deux chaînes et retourne une nouvelle chaîne.<br/>                                                     |
| [**opérateur + =**](chstring--operator-plus-equal.md)                                                | Concatène une nouvelle chaîne à la fin d’une chaîne existante.<br/>                                            |
| [**< d’opérateur (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))            | Compare un **CHString** à un **LPCWSTR**.<br/>                                                            |
| [**< d’opérateur (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))          | Compare deux **CHStrings**.<br/>                                                                            |
| [**<opérateur = (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))    | Compare deux **CHStrings**.<br/>                                                                            |
| [**<opérateur = (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))      | Compare un **CHString** à un **LPCWSTR**.<br/>                                                            |
| [**opérateur =**](chstring--operator-equal.md)                                                      | Assigne une nouvelle valeur à une chaîne **CHString** .<br/>                                                          |
| [**opérateur = = (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))          | Compare l’égalité de deux **CHStrings** .<br/>                                                               |
| [**opérateur = = (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))            | Compare un **CHString** avec un **LPCWSTR** pour vérifier l’égalité.<br/>                                               |
| [**> d’opérateur (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))       | Compare deux **CHStrings**.<br/>                                                                            |
| [**> d’opérateur (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))         | Compare un **CHString** à un **LPCWSTR**.<br/>                                                            |
| [**>opérateur = (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)) | Compare deux **CHStrings**.<br/>                                                                            |
| [**>opérateur = (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))   | Compare un **CHString** à un **LPCWSTR**.<br/>                                                            |
| [**LPCWSTR, opérateur**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)                                               | Accède directement aux caractères stockés dans une chaîne **CHString** sous la forme d’une chaîne de style C.<br/>                      |



 

## <a name="remarks"></a>Notes

Le destructeur de la classe est **CHString :: ~ CHString**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>ChString. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |




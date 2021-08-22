---
description: Contient des informations sur un formulaire d’impression localisable.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Structure FORM_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: fd933bf0ace6f394a801ab8dc4ef1fa30344b47966c09865a3aa4b713c6f2ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971518"
---
# <a name="form_info_2-structure"></a>Structure des informations de formulaire \_ \_ 2

Contient des informations sur un formulaire d’impression localisable.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a>Membres

<dl> <dt>

**Indicateurs**
</dt> <dd>

Propriétés du formulaire. Les valeurs suivantes sont définies, mais une seule peut être définie. Lorsque les **informations de formulaire \_ \_ 2** sont retournées par [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md), **Flags** est défini sur la valeur actuelle dans la base de données de formulaires.



| Valeur         | Signification                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| utilisateur de formulaire \_    | Si cet indicateur de bit est défini, le formulaire a été défini par l’utilisateur. Les formulaires avec cet indicateur défini sont définis dans le registre.                                                                                                                                                                    |
| FORMULAIRE \_ BuiltIn | Si cet indicateur de bit est défini, le formulaire fait partie du spouleur. Les définitions de formulaire pour lesquelles cet indicateur est défini n’apparaissent pas dans le registre. Les formulaires intégrés ne peuvent pas être modifiés. cet indicateur ne doit donc pas être défini lorsque la structure est transmise à [**AddForm**](addform.md) ou [**SetForm**](setform.md). |
| imprimante de formulaire \_ | Si cet indicateur de bit est défini, le formulaire est associé à une certaine imprimante et sa définition apparaît dans le registre.                                                                                                                                                                      |



 

</dd> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du formulaire. Le nom du formulaire ne peut pas dépasser 31 caractères.

</dd> <dt>

**Taille**
</dt> <dd>

Largeur et hauteur du formulaire en millièmes de millimètres.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Largeur et hauteur, en millièmes de millimètres, de la zone de la page sur laquelle l’imprimante peut imprimer.

</dd> <dt>

**pKeyword**
</dt> <dd>

Pointeur vers un identificateur de chaîne non localisable sous la forme. Lorsqu’elle est transmise à [**AddForm**](addform.md) ou [**SetForm**](setform.md), l’appelant est un moyen d’identifier le formulaire dans tous les paramètres régionaux.

</dd> <dt>

**StringType**
</dt> <dd>

Spécifie comment un nom complet localisé pour le formulaire est obtenu au moment de l’exécution. Les valeurs suivantes sont définies. Une seule peut être définie dans un appel donné à [**AddForm**](addform.md) ou [**SetForm**](setform.md). Les chaînes \_ MUIDLL et String \_ LANGPAIR peuvent être définies dans les **informations de formulaire \_ \_ 2** retournées par [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md). Consultez la section Notes.



| Valeur            | Signification                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CHAÎNE \_ aucun     | Il n’existe aucun nom complet localisé.                                                                                                                                                            |
| CHAÎNE \_ MUIDLL   | le nom d’affichage est extrait de la [interface utilisateur multilingue](/windows/desktop/Intl/mui-resource-management) DLL de ressources localisées spécifiée dans **pMuiDll**. L’ID se trouve dans le membre **dwResourceId** . |
| CHAÎNE \_ LANGPAIR | Le nom d’affichage et l’ID de langue sont fournis directement par **pDisplayName** et la langue est spécifiée par **wLangId**.                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

[interface utilisateur multilingue](/windows/desktop/Intl/mui-resource-management) DLL de ressource localisée qui contient le nom complet localisé.

</dd> <dt>

**dwResourceId**
</dt> <dd>

ID de ressource du nom d’affichage du formulaire dans **pMuiDll**.

</dd> <dt>

**pDisplayName**
</dt> <dd>

Nom complet du formulaire dans la langue spécifiée par **wLangId**.

</dd> <dt>

**wLangId**
</dt> <dd>

Langage du **pDisplayName**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Sur un appel à [**AddForm**](addform.md) ou [**SetForm**](setform.md):

-   Si **StringType** a la \_ valeur String None, **pMuiDll** et **PDisplayName** doivent tous deux avoir la **valeur null** et **dwResourceId** et **wLangId** doivent avoir la valeur 0.
-   Si **StringType** est de type String \_ MUIDLL, **PDisplayName** doit avoir la **valeur null** et **wLangId** doit avoir la valeur 0.
-   Si **StringType** est de type String \_ LANGPAIR, **PMuiDll** doit avoir la **valeur null** et **dwResourceId** doit avoir la valeur 0.

Pour les **informations de formulaire \_ \_ 2** retournées par un appel à [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md):

-   Si **StringType** est à la fois String \_ MUIDLL et String \_ LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId** et **wLangId** auront des valeurs valides.
-   Si **StringType** a la valeur String \_ MUIDLL only, **pMuiDll** et **dwResourceId** auront des valeurs valides. **pDisplayName** sera **null** et **wLangId** sera 0.
-   Si **StringType** a la valeur String \_ LANGPAIR only, **pDisplayName** et **wLangId** auront des valeurs valides. **pMuiDll** sera **null** et **dwResourceId** sera 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ Informations de formulaire \_ \_ 2S** (Unicode) et **\_ informations de formulaire \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[Interface utilisateur multilingue](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 


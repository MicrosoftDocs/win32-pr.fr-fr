---
description: Contient des informations sur la boîte de dialogue affichée par la fonction CryptUIDlgSelectCertificate.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: Structure CRYPTUI_SELECTCERTIFICATE_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520766"
---
# <a name="cryptui_selectcertificate_struct-structure"></a>\_SELECTCERTIFICATE \_ structure de struct CRYPTUI

La structure du **\_ \_ struct CRYPTUI SELECTCERTIFICATE** contient des informations sur la boîte de dialogue affichée par la fonction [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

Taille, en octets, de cette structure.

</dd> <dt>

**hwndParent**
</dt> <dd>

Handle de la fenêtre parente de la boîte de dialogue. Si cette valeur est **null**, la fenêtre parente est la fenêtre du bureau par défaut.

</dd> <dt>

**dwFlags**
</dt> <dd>

Spécifie des options supplémentaires pour la fonction [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) . Il peut s’agir de **zéro ou d’une opération or** au niveau du bit des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt> </dl>                              | Réservé.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ hérité**</dt> </dl>                                       | Spécifie que la boîte de dialogue héritée doit être affichée.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <dt>**\_présélection SELECTCERT CRYPTUI \_**</dt> </dl>                        | Permet à l’utilisateur de sélectionner plusieurs certificats dans la boîte de dialogue. Si cet indicateur est défini, la fonction [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) retourne toujours la **valeur null**. Le membre **hSelectedCertStore** de cette structure doit contenir un handle vers un magasin de certificats. Les certificats sélectionnés par l’utilisateur sont ajoutés à ce magasin.<br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ put \_ WindowsT \_**</dt> </dl> | Force l’interface utilisateur de chiffrement à être la fenêtre supérieure à l’écran.<br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**szTitle**
</dt> <dd>

Titre d’affichage de la boîte de dialogue. Si la valeur de ce membre est **null**, le titre par défaut « sélectionner un certificat » est utilisé.

</dd> <dt>

**dwDontUseColumn**
</dt> <dd>

Indicateurs qui peuvent être combinés pour exclure des colonnes de l’affichage.



| Valeur                                                                                                                                                                                                                                                                                       | Signification                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <dt>**CRYPTUI \_ Sélectionnez \_ IssuedTo, \_ colonne**</dt> <dt>1 (0x1)</dt> </dl>             | N’affiche pas d’informations **IssuedTo,** .<br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <dt>**CRYPTUI \_ Sélectionnez \_ la \_ colonne IssuedBy,**</dt> <dt>2 (0X2)</dt> </dl>             | N’affiche pas d’informations **IssuedBy,** .<br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <dt>**CRYPTUI \_ SÉLECTIONNER \_ la \_ colonne INTENDEDUSE**</dt> <dt>4 (0x4)</dt> </dl>    | N’affiche pas d’informations **IntendedUse** .<br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <dt>**CRYPTUI \_ Sélectionnez \_ la \_ colonne FRIENDLYNAME**</dt> <dt>8 (0x8)</dt> </dl> | N’affiche pas d’informations sur le nom.<br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <dt>**CRYPTUI \_ SÉLECTIONNER l' \_ emplacement \_ colonne**</dt> <dt>16 (0x10)</dt> </dl>           | N’affiche pas les informations relatives à l’emplacement.<br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <dt>**CRYPTUI \_ Sélectionnez \_ la \_ colonne d’expiration**</dt> <dt>32 (0x20)</dt> </dl>     | N’affiche pas les informations d’expiration.<br/>      |



 

</dd> <dt>

**szDisplayString**
</dt> <dd>

Texte affiché dans la boîte de dialogue pour indiquer à l’utilisateur. Si la valeur de ce membre est **null**, la chaîne par défaut « sélectionner un certificat que vous souhaitez utiliser » est utilisée.

</dd> <dt>

**pFilterCallback**
</dt> <dd>

Pointeur vers une fonction de rappel [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) qui filtre les certificats affichés dans la boîte de dialogue.

</dd> <dt>

**pDisplayCallback**
</dt> <dd>

Pointeur vers une fonction de rappel [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) qui affiche les certificats que l’utilisateur sélectionne pour afficher.

</dd> <dt>

**pvCallbackData**
</dt> <dd>

Données supplémentaires passées aux fonctions de rappel spécifiées par les membres **pFilterCallback** et **pDisplayCallback** .

</dd> <dt>

**cDisplayStores**
</dt> <dd>

Nombre de magasins de certificats dans le tableau **rghDisplayStores** .

</dd> <dt>

**rghDisplayStores**
</dt> <dd>

Pointeur vers un tableau de magasins qui contiennent des certificats disponibles pour la sélection dans la boîte de dialogue.

</dd> <dt>

**cStores**
</dt> <dd>

Nombre de magasins de certificats dans le tableau **rghStores** .

</dd> <dt>

**rghStores**
</dt> <dd>

Pointeur vers un tableau de magasins de certificats à rechercher lors de la création d’une chaîne de certificats et de la vérification de l’approbation pour les certificats affichés dans la boîte de dialogue.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Nombre de pages de propriétés dans le tableau **rgPropSheetPages** .

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Pointeur vers un tableau de structures **PROPSHEETPAGE** qui représentent les pages de propriétés qui sont passées à la boîte de dialogue d’affichage du certificat lorsqu’un certificat est sélectionné pour l’affichage.

</dd> <dt>

**hSelectedCertStore**
</dt> <dd>

Handle d’un magasin de certificats créé par l’appelant. Les certificats sélectionnés par l’utilisateur sont ajoutés à ce magasin. Si le nombre de certificats dans ce magasin est identique avant et après l’appel de [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), l’utilisateur a fermé la boîte de dialogue sans sélectionner de certificats.

Ce membre n’est pas utilisé si le membre **dwFlags** de cette structure ne contient pas l’indicateur **\_ \_ MultiSelect CRYPTUI SELECTCERT** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                            |
| Noms Unicode et ANSI<br/>   | **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) et **CRYPTUI \_ SELECTCERTIFICATE \_ structa** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 





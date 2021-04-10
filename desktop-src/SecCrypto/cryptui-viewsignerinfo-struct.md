---
description: Contient des informations pour la fonction CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Structure CRYPTUI_VIEWSIGNERINFO_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034504"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a>\_VIEWSIGNERINFO \_ structure de struct CRYPTUI

\[La structure du **\_ \_ struct CRYPTUI VIEWSIGNERINFO** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

La structure du **\_ \_ struct CRYPTUI VIEWSIGNERINFO** contient des informations pour la fonction [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .

> [!Note]  
> Cette structure n’est pas déclarée dans un fichier d’en-tête publié. Pour utiliser cette structure, déclarez-la dans le format exact indiqué.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

Taille, en octets, de cette structure.

</dd> <dt>

**hwndParent**
</dt> <dd>

Handle de la fenêtre qui doit être le parent de la boîte de dialogue. Ce membre peut avoir la **valeur null** si la boîte de dialogue ne doit pas avoir de parent.

</dd> <dt>

**dwFlags**
</dt> <dd>

Jeu d’indicateurs qui modifie le comportement de la fonction [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) . Aucun indicateur n’est actuellement défini. ce membre doit donc être égal à zéro.

</dd> <dt>

**szTitle**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le titre à afficher dans la boîte de dialogue. Si ce membre a la **valeur null**, un titre par défaut est utilisé.

</dd> <dt>

**pSignerInfo**
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ informations du signataire CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) qui contient les informations sur le signataire à afficher.

</dd> <dt>

**hMsg**
</dt> <dd>

Handle du message à partir duquel les informations du signataire ont été extraites.

</dd> <dt>

**pszOID**
</dt> <dd>

Pointeur vers une chaîne ANSI se terminant par un caractère null qui contient la représentation sous forme de chaîne de l' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) qui indique le certificat pour lequel la signature doit être validée. Par exemple, si cette méthode est appelée pour afficher la signature d’une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL), la chaîne d’OID de **\_ \_ \_ \_ signature d’utilisation szOID KP** doit être transmise. Si ce membre a la **valeur null**, le certificat n’est pas validé pour les utilisations.

</dd> <dt>

**dwReserved**
</dt> <dd>

Ce paramètre n’est pas utilisé actuellement. Ce membre doit avoir la **valeur null**.

</dd> <dt>

**cStores**
</dt> <dd>

Nombre d’éléments dans le tableau **rghStores** .

</dd> <dt>

**rghStores**
</dt> <dd>

Tableau de valeurs **HCERTSTORE** qui représentent les autres magasins de certificats pour rechercher le certificat qui a signé le message. Si ce membre a la **valeur null**, aucun autre magasin n’est recherché. Le membre **cStores** contient le nombre d’éléments de ce tableau.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Nombre d’éléments dans le tableau **rgPropSheetPages** .

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Tableau de pointeurs de structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) qui définissent les pages supplémentaires à afficher dans la boîte de dialogue standard. Si ce membre a la **valeur null**, aucune page supplémentaire ne sera affichée. Le membre **cPropSheetPages** contient le nombre d’éléments de ce tableau.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                      |
| Noms Unicode et ANSI<br/>   | **CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) et **CRYPTUI \_ VIEWSIGNERINFO \_ structa** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 

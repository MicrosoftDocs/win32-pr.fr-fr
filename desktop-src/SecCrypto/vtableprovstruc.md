---
description: Contient des pointeurs vers des fonctions de rappel qui peuvent être utilisées par les fonctions du fournisseur de services de chiffrement (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: VTableProvStruc, structure (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759459"
---
# <a name="vtableprovstruc-structure"></a>VTableProvStruc, structure

La structure **VTableProvStruc** contient des pointeurs vers des fonctions de rappel qui peuvent être utilisées par les fonctions du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Valeur **DWORD** qui indique la version de la structure. Trois versions de cette structure sont utilisées. Les versions sont les numéros 1, 2 et 3, et déterminent les membres de la structure qui sont valides. Les membres de la version 1 sont valides sur tous les systèmes qui prennent en charge cette structure.

Il s’agit d’un membre de la version 1.

</dd> <dt>

**FuncVerifyImage**
</dt> <dd>

Adresse d’une fonction de rappel [**FuncVerifyImage**](funcverifyimage.md) que le CSP utilise pour vérifier la signature des dll que le CSP chargera. Toutes les dll auxiliaires dans lesquelles un CSP effectue des appels de fonction doivent être signées de la même manière (et avec la même clé) que la DLL CSP principale. Pour garantir cette signature, les dll auxiliaires doivent être chargées de manière dynamique à l’aide de la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Mais avant le chargement de la DLL, la signature de la DLL doit être vérifiée. Le fournisseur CSP effectue cette vérification en appelant la fonction **FuncVerifyImage** , comme illustré dans l’exemple ci-dessous.

Ce pointeur de fonction peut être stocké et utilisé jusqu’à ce que le contexte CSP soit libéré.

Il s’agit d’un membre de la version 1.

</dd> <dt>

**FuncReturnhWnd**
</dt> <dd>

Adresse d’une fonction de rappel [**FuncReturnhWnd**](funcreturnhwnd.md) qui retourne le handle de fenêtre que le fournisseur de services Cloud doit utiliser comme parent ou propriétaire d’une interface utilisateur qui est affichée. Les fournisseurs de services de chiffrement qui ne communiquent pas directement avec l’utilisateur et les fournisseurs de services de chiffrement qui utilisent du matériel dédié à cet effet peuvent ignorer cette entrée. Par défaut, ce handle de fenêtre est égal à zéro, mais une application peut définir cette valeur sur une autre valeur à l’aide de la fonction [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) pour définir la propriété **\_ \_ HWND du client pp** .

Ce pointeur de fonction peut être stocké et utilisé jusqu’à ce que le contexte CSP soit libéré.

Il s’agit d’un membre de la version 1.

</dd> <dt>

**dwProvType**
</dt> <dd>

Valeur **DWORD** qui spécifie le type de fournisseur à acquérir. Les [*types de fournisseurs*](../secgloss/p-gly.md) suivants sont prédéfinis et sont décrits en détail dans [interopérabilité des fournisseurs de services](https://www.bing.com/search?q=CSP+Interoperability)Cloud :

-   PROUVER \_ RSA \_ Full
-   PROUVER \_ RSA \_ SIG
-   DSS PROVen \_
-   \_Fortezza-Fortezza
-   PROUVER \_ MS \_ Exchange

Il s’agit d’un membre de la version 2.

</dd> <dt>

**pbContextInfo**
</dt> <dd>

Pointeur vers un tableau d’informations de contexte. Les membres **pbContextInfo** et **cbContextInfo** déterminent ensemble le jeu d’informations utilisé quand une fonction [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) est appelée avec les informations de \_ contexte pp \_ définies.

Il s’agit d’un membre de la version 2.

</dd> <dt>

**cbContextInfo**
</dt> <dd>

Valeur **DWORD** qui indique le nombre d’éléments dans le tableau **pbContextInfo** .

Il s’agit d’un membre de la version 2.

</dd> <dt>

**pszProvName**
</dt> <dd>

Chaîne qui contient le nom du fournisseur.

Il s’agit d’un membre de la version 3.

</dd> </dl>

## <a name="remarks"></a>Notes

Les pointeurs de la structure **VTableProvStruc** sont uniquement disponibles dans la fonction [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) . Si des membres de la structure sont nécessaires après l’exécution d’un appel à **CPAcquireContext** , des copies des éléments de structure nécessaires doivent être effectuées par le CSP. Les pointeurs de fonction de cette structure peuvent être stockés et utilisés jusqu’à ce que le contexte du CSP soit libéré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **VTableProvStrucW** (Unicode)<br/>                                          |



 

 

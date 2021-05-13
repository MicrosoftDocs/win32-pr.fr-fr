---
description: Crée un tableau de handles pour les icônes extraites d’un fichier spécifié.
title: SHExtractIconsW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840910"
---
# <a name="shextracticonsw-function"></a>SHExtractIconsW fonction)

\[**SHExtractIconsW** est disponible via Windows XP Service Pack 2 (SP2). Il peut être modifié ou non disponible dans les versions ultérieures.\]

Crée un tableau de handles pour les icônes extraites d’un fichier spécifié.

## <a name="syntax"></a>Syntaxe


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszFileName* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers le nom de fichier à partir duquel extraire les icônes.

</dd> <dt>

*nIconIndex* \[ dans\]
</dt> <dd>

Type : **int**

Index de la première icône à extraire de la ressource nommée dans *pszFileName*.

</dd> <dt>

*cxIcon* \[ dans\]
</dt> <dd>

Type : **int**

Largeur souhaitée de l’icône. Consultez la section Notes.

</dd> <dt>

*cyIcon* \[ dans\]
</dt> <dd>

Type : **int**

Hauteur souhaitée de l’icône. Consultez la section Notes.

</dd> <dt>

*phIcon* \[ à\]
</dt> <dd>

Type : **HICON \***

Lorsque cette fonction est retournée, contient un pointeur vers le tableau de handles d’icône.

</dd> <dt>

*pIconId* \[ à\]
</dt> <dd>

Type : **uint \***

Lorsque cette fonction est retournée, contient un pointeur vers l’identificateur de ressource de l’icône extraite qui correspond le mieux au périphérique d’affichage actuel. Si aucun identificateur n’est disponible pour ce format, il contient 0xFFFFFFFF. Si aucun identificateur ne peut être obtenu pour une autre raison, retourne la valeur zéro.

</dd> <dt>

*nIcons* \[ dans\]
</dt> <dd>

Type : **uint**

Nombre d’icônes à extraire de la ressource nommée dans *pszFileName*. Ce paramètre est valide uniquement lorsque la ressource est un fichier. exe ou. dll.

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Type : **uint**

Indicateurs qui contrôlent cette fonction. Pour connaître les valeurs possibles, consultez le paramètre *fuLoad* de la fonction [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **uint**

Valeur différente de zéro en cas de réussite ; Sinon, zéro.

## <a name="remarks"></a>Notes

**SHExtractIconsW** extrait des types de fichiers suivants.

-   Fichier exécutable (.exe)
-   DLL (. dll)
-   Icône (. ico)
-   Curseur (. cur)
-   Curseur animé (. ani)
-   Bitmap (.bmp)

Extractions à partir de Windows 3. *x* les fichiers exécutables 16 bits (. exe ou. dll) sont également pris en charge.

Les paramètres *cxIcon* et *cyIcon* spécifient la taille des icônes à extraire. Deux tailles peuvent être extraites par le biais de chaque paramètre en fractionnant la valeur entre ses LOWORD et HIWORD. Placez la première taille souhaitée dans le LOWORD du paramètre et la deuxième taille dans le HIWORD. Par exemple, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) pour *cxIcon* et *cyIcon* extrait les icônes 24 et 48.

Le processus appelant est responsable de la destruction de toutes les icônes extraites par le biais de cette fonction en appelant la fonction [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) .

**SHExtractIconsW** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public. Pour l’utiliser, vous devez déclarer un prototype correspondant et utiliser [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour demander un pointeur de fonction à partir de Shell32.dll qui peut être utilisé pour appeler cette fonction.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **SHExtractIconsW** (Unicode)<br/>                                                                      |



 

 

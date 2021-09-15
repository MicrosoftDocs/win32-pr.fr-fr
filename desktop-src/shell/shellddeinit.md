---
description: inscrit les services de l’échange dynamique de données interpréteur de commandes (DDE) dans le processus en cours, en avertissant le système que le processus en cours souhaite héberger des objets DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412370"
---
# <a name="shellddeinit-function"></a>ShellDDEInit fonction)

inscrit les services de l’échange dynamique de données interpréteur de commandes (DDE) dans le processus en cours, en avertissant le système que le processus en cours souhaite héberger des objets DDE.

## <a name="syntax"></a>Syntaxe


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*init* \[ dans\]
</dt> <dd>

Type : **bool**

**True** pour inscrire le processus en cours en tant qu’hôte DDE ; **False** pour annuler son inscription.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le processus qui appelle cette fonction agit en tant qu’interpréteur de commandes et est utilisé pour afficher le contenu des dossiers ouverts avec le verbe « Open » [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

Cette fonction n’a pas de fichier d’en-tête ou de bibliothèque associé et doit donc être appelée par valeur ordinale. Appelez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Shdocvw.dll) pour obtenir un handle de module. Appelez ensuite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le numéro ordinal de fonction 118 pour récupérer l’adresse de la fonction.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP, Windows 2000 Professional \[ applications de bureau uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shdocvw.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

 

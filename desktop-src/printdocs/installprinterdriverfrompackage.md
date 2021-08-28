---
description: Installe un pilote d’imprimante à partir d’un package de pilotes qui se trouve dans le magasin de pilotes des serveurs d’impression.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: InstallPrinterDriverFromPackage, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 3248fc1a2392e2a04fd83c58ddcc08a110eec94779b634ce6a348639d4d2a5c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112469"
---
# <a name="installprinterdriverfrompackage-function"></a>InstallPrinterDriverFromPackage fonction)

Installe un pilote d’imprimante à partir d’un package de pilotes qui se trouve dans le magasin de pilotes du serveur d’impression.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression. La **valeur null** correspond à l’ordinateur local.

</dd> <dt>

*pszInfPath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le chemin d’accès du magasin de pilotes au fichier. inf du pilote d’impression. **Null** signifie que le pilote se trouve dans un fichier INF fourni avec Windows.

</dd> <dt>

*pszDriverName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du pilote.

</dd> <dt>

*pszEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86). Il peut s’agir de la **valeur null**.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce peut être uniquement 0 ou IPDFP \_ copier \_ tous les \_ fichiers. La valeur 0 signifie que le pilote d’imprimante doit être ajouté et que tous les fichiers du répertoire du pilote d’imprimante qui sont plus récents que les fichiers correspondants en cours d’utilisation doivent être copiés. La valeur IPDFP \_ copier \_ tous les \_ fichiers signifie que le pilote d’imprimante et tous les fichiers du répertoire du pilote d’imprimante doivent être ajoutés. Les horodatages de fichier sont ignorés quand *dwFlags* a la valeur IPDFP \_ copier \_ tous les \_ fichiers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.

Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Le magasin de pilotes est généralement% windir% \\ INF ou% windir% \\ system32 \\ DriverStore \\ FileRepository.

**InstallPrinterDriverFromPackage** installe également d’autres fichiers dans le package, tels que les profils de couleurs et les processeurs d’impression.

Les utilisateurs doivent disposer de droits d’administration d’imprimante pour installer sur un ordinateur distant ou sur l’ordinateur local lorsque l’utilisateur est connecté avec les services Terminal Server.

Seuls les packages signés peuvent être installés sur un ordinateur distant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Noms Unicode et ANSI<br/>   | **InstallPrinterDriverFromPackageW** (Unicode) et **InstallPrinterDriverFromPackageA** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 


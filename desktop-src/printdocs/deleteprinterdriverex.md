---
description: La fonction DeletePrinterDriverEx supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur et supprime les fichiers associés au pilote. Cette fonction peut également supprimer des versions spécifiques du pilote.
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: DeletePrinterDriverEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293438"
---
# <a name="deleteprinterdriverex-function"></a>DeletePrinterDriverEx fonction)

La fonction **DeletePrinterDriverEx** supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur et supprime les fichiers associés au pilote. Cette fonction peut également supprimer des versions spécifiques du pilote.

## <a name="syntax"></a>Syntaxe


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur à partir duquel le pilote doit être supprimé. Si ce paramètre a la **valeur null**, la fonction supprime le pilote d’imprimante de l’ordinateur local.

</dd> <dt>

*pEnvironment* \[ dans\]
</dt> <dd>

pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le pilote doit être supprimé (par exemple, Windows NT x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, le nom du pilote est supprimé de l’environnement actuel de l’application appelante et de l’ordinateur client (et non de l’application de destination et du serveur d’impression).

</dd> <dt>

*pDriverName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote à supprimer.

</dd> <dt>

*dwDeleteFlag* \[ dans\]
</dt> <dd>

Options permettant de supprimer des fichiers et des versions du pilote. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                     | Signification                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <dt>**MORT \_ supprimer \_ une \_ version spécifique**</dt> </dl> | Supprime la version spécifiée dans *dwVersionFlag*. Cela ne garantit pas que le pilote sera supprimé de la liste des pilotes pris en charge pour le serveur.<br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <dt>**MORT \_ Supprimer les \_ fichiers inutilisés \_**</dt> </dl>             | Supprime tous les fichiers de pilote inutilisés.<br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <dt>**MORT \_ supprimer \_ tous les \_ fichiers**</dt> </dl>                      | Supprime le pilote uniquement si tous ses fichiers associés peuvent être supprimés. L’opération de suppression échoue si l’un des fichiers du pilote est utilisé par un autre pilote installé.<br/> |



 

Si mort \_ supprimer \_ une \_ version spécifique n’est pas spécifié, la fonction supprime toutes les versions du pilote si aucune d’entre elles n’est en cours d’utilisation. Si ni mort \_ supprimer \_ les fichiers inutilisés \_ , ni mort \_ supprimer \_ tous les \_ fichiers n’est spécifié, la fonction ne supprime pas les fichiers de pilote.

</dd> <dt>

*dwVersionFlag* \[ dans\]
</dt> <dd>

Version du pilote à supprimer. Ce paramètre peut avoir la valeur 0, 1, 2 ou 3. Ce paramètre est utilisé uniquement si *dwDeleteFlag* comprend l' \_ indicateur mort supprimer la \_ \_ version spécifique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Avant de supprimer les fichiers de pilote, la fonction appelle la fonction **DrvDriverEvent** du pilote, ce qui permet au pilote de supprimer tous les fichiers privés qui ne sont pas utilisés. pour plus d’informations sur **DrvDriverEvent**, consultez le kit de développement de pilotes (DDK) Microsoft Windows.

Si les fichiers de pilote sont actuellement chargés, la fonction les déplace vers un répertoire temporaire et les marque pour la suppression au redémarrage.

Avant d’appeler **DeletePrinterDriverEx**, vous devez supprimer tous les objets d’imprimante qui utilisent le pilote d’imprimante.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **DeletePrinterDriverExW** (Unicode) et **DeletePrinterDriverExA** (ANSI)<br/>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

 





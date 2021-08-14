---
description: La fonction AddPrinterDriverEx installe un pilote d’imprimante local ou distant et lie les fichiers de configuration, de données et de pilote.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: AddPrinterDriverEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 00bd65ad415a97bbab825e4a13c8ad985d1d7f9b79d7b46e3f8f7ea6b5e5f0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868808"
---
# <a name="addprinterdriverex-function"></a>AddPrinterDriverEx fonction)

La fonction **AddPrinterDriverEx** installe un pilote d’imprimante local ou distant et lie les fichiers de configuration, de données et de pilote. Outre les fonctionnalités de [**AddPrinterDriver**](addprinterdriver.md), il offre également des options qui permettent une mise à niveau stricte, une rétrogradation stricte, la copie de fichiers récents uniquement et la copie de tous les fichiers (quels que soient les horodatages des fichiers).

> [!Note]  
> L’installation d’un pilote d’imprimante sans package de pilotes n’est plus recommandée. Utilisez [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) à la place.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le pilote doit être installé. Si ce paramètre a la **valeur null**, la fonction installe le pilote sur l’ordinateur local.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure vers laquelle *pDriverInfo* pointe. Cette valeur peut être 2, 3, 4, 6 ou 8.

</dd> <dt>

*pDriverInfo* \[ in, out\]
</dt> <dd>

Pointeur vers une structure contenant des informations sur le pilote d’imprimante. Il peut s’agir de l’une des valeurs suivantes.



| Valeur de niveau                                                                                       | \_Structure info \_ du pilote \*                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**\_Informations sur le pilote \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**\_Informations sur le pilote \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**\_Informations sur le pilote \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**\_Informations sur le pilote \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**\_Informations sur le pilote \_ 8**](driver-info-8.md)<br/> |



 

Si le membre **pEnvironment** de la structure vers laquelle pointe *PDriverInfo* a la **valeur null**, la fonction utilise l’environnement actuel de l’appelant/du client, et non de l’environnement du serveur de destination/serveur.

</dd> <dt>

*dwFileCopyFlags* \[ dans\]
</dt> <dd>

Options de copie des fichiers de pilote. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**APD \_ copier \_ tous les \_ fichiers**</dt> </dl>                | Ajoutez le pilote d’imprimante et copiez tous les fichiers dans le répertoire du pilote d’imprimante. Les horodatages de fichier sont ignorés avec cette option.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**APD \_ copier \_ à partir de l' \_ Annuaire**</dt> </dl> | Ajoutez le pilote d’imprimante à l’aide des noms de fichiers complets spécifiés dans la structure [**\_ info \_ 6 du pilote**](driver-info-6.md) . Cet indicateur est associé à l’un des autres indicateurs de copie. Si cet indicateur est défini, **AddPrinterDriverEx** échoue si les fichiers n’existent pas là où ils sont spécifiés pour exister dans la structure **\_ information \_ 6 du pilote** . Les fichiers ne doivent pas être copiés dans le répertoire du pilote d’imprimante du système. Consultez les notes.<br/> **Windows 2000 :** Cet indicateur n’est pas pris en charge.<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**APD \_ copier les \_ nouveaux \_ fichiers**</dt> </dl>                | Ajoutez le pilote d’imprimante et copiez les fichiers du répertoire du pilote d’imprimante qui sont plus récents que les fichiers correspondants en cours d’utilisation. Cet indicateur émule le comportement de [**AddPrinterDriver**](addprinterdriver.md).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**\_rétrogradation stricte APD \_**</dt> </dl>           | Ajoutez le pilote d’imprimante uniquement si tous les fichiers du répertoire du pilote d’imprimante sont antérieurs aux fichiers correspondants en cours d’utilisation.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**\_ \_ mise à niveau STRICTe APD**</dt> </dl>                 | Ajoutez le pilote d’imprimante uniquement si tous les fichiers du répertoire du pilote d’imprimante sont plus récents que les fichiers correspondants en cours d’utilisation.<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

Si le pilote d’imprimante rencontre des problèmes de fonctionnement avec le système d’exploitation, **AddPrinterDriverEx** échoue avec l’un des codes d’erreur suivants :



| Code d'erreur                      | Signification                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERREUR \_ de \_ pilote d’imprimante \_ bloquée | Le pilote ne fonctionne pas sur le système d’exploitation.                                                                                                         |
| ERREUR \_ de \_ pilote d’imprimante \_  | Le pilote n’est pas fiable sur le système d’exploitation. Toutefois, si \_ le pilote d’installation APD \_ \_ est spécifié, le pilote est installé et aucun avertissement n’est fourni. |



 

Pour plus d'informations, consultez la section Notes.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Avant d’appeler la fonction **AddPrinterDriverEx** , tous les fichiers requis par le pilote doivent être copiés dans le répertoire du pilote d’imprimante du système. Pour récupérer le nom de ce répertoire, appelez la fonction [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .

Pour déterminer les pilotes d’imprimante actuellement installés, appelez la fonction [**EnumPrinterDrivers**](enumprinterdrivers.md) .

Si le pilote d’imprimante a été ajouté avec succès, la fonction appelle la fonction DrvDriverEvent (DRIVER \_ Event \_ Initialize, Level, Driver \_ info \_ \* , lParam) pour permettre au pilote d’effectuer les initialisations nécessaires pendant l’installation d’un pilote d’imprimante. pour plus d’informations sur **DrvDriverEvent**, consultez le kit de développement de pilotes (DDK) Microsoft Windows

Le pilote ne doit pas utiliser un appel d’interface utilisateur lors de l’appel à **DrvDriverEvent**. Pour effectuer des tâches liées à l’interface utilisateur, le programme d’installation doit utiliser l’entrée VendorSetup dans le fichier. inf de l’imprimante ou, pour Plug-and-Play appareils, le programme d’installation peut utiliser un co-programme d’installation spécifique à l’appareil. Pour plus d’informations sur VendorSetup, consultez le DDK.

Les fichiers qui sont référencés dans la [**structure \_ info \_ 6 du pilote**](driver-info-6.md) doivent être locaux sur l’ordinateur à partir duquel l’appel est effectué. Un nom de fichier peut être un nom UNC tant que le nom UNC est l’ordinateur local.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AddPrinterDriverExW** (Unicode) et **AddPrinterDriverExA** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 2**](driver-info-2.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 3**](driver-info-3.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 4**](driver-info-4.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 6**](driver-info-6.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 


---
description: Supprime un package d’exception.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: UninstallComponent fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: d6b4ce8e447bc884d1b3ee64505d230b2e069ce6cda1630b027b8a48da68beda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001109"
---
# <a name="uninstallcomponent-function"></a>UninstallComponent fonction)

Supprime un package d’exception.

## <a name="syntax"></a>Syntaxe


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CompGuid* \[ dans, facultatif\]
</dt> <dd>

GUID du composant d’exception en cours de désinstallation.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Indicateurs utilisés pour contrôler les comportements d’installation. Ce paramètre peut être une combinaison des valeurs suivantes.



| Valeur                                                                                                                                                                                                         | Signification                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**\_indicateurs COMP \_ noui**</dt> </dl>                                          | Supprime toute l’interface utilisateur.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**\_ \_ mise à jour dllcache des indicateurs COMP \_**</dt> </dl>        | Force la mise à jour du répertoire DLLCACHE lorsqu’un fichier système est mis à jour.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**les \_ indicateurs COMP \_ utilisent le \_ \_ cache SVCPACK**</dt> </dl> | utilise les fichiers mis en cache par un Windows Service Pack installer pour remplacer les fichiers sauvegardés.<br/> |



 

</dd> <dt>

*VerMajor* \[ dans, facultatif\]
</dt> <dd>

Version principale du composant d’exception à désinstaller.

</dd> <dt>

*Vermine* \[ dans, facultatif\]
</dt> <dd>

Version mineure du composant d’exception à désinstaller.

</dd> <dt>

*VerBuild* \[ dans, facultatif\]
</dt> <dd>

Version de build du composant d’exception à désinstaller.

</dd> <dt>

*VerQFE* \[ dans, facultatif\]
</dt> <dd>

Révision du correctif logiciel du composant d’exception à désinstaller.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

les packages d’Exception sont Windows les fichiers système qui sont publiés en dehors d’un package complet Windows version et qui mettent à jour les fichiers du système d’exploitation. les packages d’Exception sont créés uniquement par les équipes du système d’exploitation qui ont reçu l’autorisation de mettre à jour Windows fichiers système.

pour installer et désinstaller des fichiers qui ne sont pas protégés par Windows Protection des fichiers, utilisez les fonctions documentées dans les [fonctions d’installation générales](https://msdn.microsoft.com/library/ms794585.aspx). Pour installer des pilotes de périphérique, les fournisseurs doivent utiliser les fonctions documentées dans [fonctions d’installation des appareils](https://msdn.microsoft.com/library/ms792954.aspx) et [fonctions PNP Configuration Manager](https://msdn.microsoft.com/library/ms790838.aspx).

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 

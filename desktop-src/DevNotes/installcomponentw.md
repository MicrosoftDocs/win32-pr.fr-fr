---
description: Installe un package d’exception.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: InstallComponentW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 9deaa460ec58ad0aa07af38aa03f53971068b4a6a1d43131e5473a7e4def908c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955918"
---
# <a name="installcomponentw-function"></a>InstallComponentW fonction)

Installe un package d’exception.

## <a name="syntax"></a>Syntaxe


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*InfPath* \[ dans\]
</dt> <dd>

Chemin d’accès à l’exception INF à traiter.

</dd> <dt>

*CompGuid* \[ dans, facultatif\]
</dt> <dd>

GUID du composant d’exception en cours d’installation.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Indicateurs utilisés pour contrôler les comportements d’installation. Ce paramètre peut être une combinaison des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                               | Signification                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**COMP \_ INDICATEURS \_ force**</dt> <dt>0x00000020</dt> </dl>                             | Ignore la vérification de la version sur les remplacements de fichiers.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**COMP \_ les indicateurs \_ doivent être \_ désinstallés**</dt><dt></dt> </dl>        | Sauvegardez les fichiers qui sont mis à jour pour être utilisés par une désinstallation du composant.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**COMP \_ INDICATEURS \_ sans \_ remplacement**</dt><dt></dt> </dl>                 | Ignore la sauvegarde des fichiers si la version du composant d’exception est identique à celle d’un composant installé. Cet indicateur est utilisé dans un scénario de réinstallation.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ INDICATEURS \_ noui**</dt> <dt>0x00000002</dt> </dl>                                | Supprime toute l’interface utilisateur.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_ INDICATEURS \_ Update \_ dllcache**</dt><dt></dt> </dl>        | Force la mise à jour du répertoire DLLCACHE lorsqu’un fichier système est mis à jour.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**COMP \_ les indicateurs \_ utilisent le \_ \_ cache SVCPACK**</dt><dt></dt> </dl> | utilise les fichiers mis en cache par un Windows Service Pack installer pour remplacer les fichiers sauvegardés.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ dans, facultatif\]
</dt> <dd>

Version principale du composant d’exception.

</dd> <dt>

*Vermine* \[ dans, facultatif\]
</dt> <dd>

Version mineure du composant d’exception.

</dd> <dt>

*VerBuild* \[ dans, facultatif\]
</dt> <dd>

Version de build du composant d’exception.

</dd> <dt>

*VerQFE* \[ dans, facultatif\]
</dt> <dd>

Révision du correctif logiciel du composant d’exception.

</dd> <dt>

*Nom* \[ dans, facultatif\]
</dt> <dd>

chaîne descriptive du composant indiquée par la boîte de dialogue Windows protection de fichier si le système d’exploitation détecte qu’un fichier protégé de protection de fichier Windows est endommagé, falsifié ou endommagé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne une valeur **HRESULT** (S \_ OK ou un code d’échec). Un code d’échec peut être vérifié par rapport à une valeur de 0x20000100 pour déterminer si l’échec est dû à un redémarrage requis.

## <a name="remarks"></a>Remarques

les packages d’Exception sont Windows les fichiers système qui sont publiés en dehors d’un package complet Windows version et qui mettent à jour les fichiers du système d’exploitation. les packages d’Exception sont créés uniquement par les équipes du système d’exploitation qui ont reçu l’autorisation de mettre à jour Windows fichiers système.

pour installer et désinstaller des fichiers qui ne sont pas protégés par Windows Protection des fichiers, utilisez les fonctions documentées dans les [fonctions d’installation générales](https://msdn.microsoft.com/library/ms794585.aspx). Pour installer des pilotes de périphérique, les fournisseurs doivent utiliser les fonctions documentées dans [fonctions d’installation des appareils](https://msdn.microsoft.com/library/ms792954.aspx) et [fonctions PNP Configuration Manager](https://msdn.microsoft.com/library/ms790838.aspx).

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 

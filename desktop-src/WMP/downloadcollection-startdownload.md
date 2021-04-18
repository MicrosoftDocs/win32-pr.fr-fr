---
title: Méthode DownloadCollection. startDownload
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode startDownload met en file d’attente un téléchargement.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- méthode startDownload lecteur Windows Media
- méthode startDownload lecteur Windows Media, classe DownloadCollection
- Classe DownloadCollection lecteur Windows Media, méthode startDownload
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528955"
---
# <a name="downloadcollectionstartdownload-method"></a>Méthode DownloadCollection. startDownload

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **startDownload** met en file d’attente un téléchargement.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sourceURL* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant l’URL du téléchargement.

</dd> <dt>

*type* \[ dans\]
</dt> <dd>

**Chaîne** spécifiant le type de téléchargement. Contient l'une des valeurs suivantes :



| Valeur      | Description                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Windows XP et versions ultérieures.) Le téléchargement se produit en tant que processus en arrière-plan, car le temps processeur devient disponible. Les États de téléchargement persistent même lorsque Windows Media Player ou Windows XP est arrêté. |
| temps réel  | (Tous les systèmes d’exploitation pris en charge.) Le téléchargement a lieu en même temps. Aucun État de téléchargement n’est conservé entre les sessions.                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet **DownloadItem** .

## <a name="remarks"></a>Notes

Lors du démarrage d’un nouveau téléchargement, le gestionnaire de téléchargement l’ajoute en tant qu’élément à la collection de téléchargements qui a initié le téléchargement.

Seuls les formats multimédias numériques suivants peuvent être téléchargés :

-   ASF (Advanced Systems Format)
-   MP3
-   Audio Windows Media (WMA)
-   Vidéo Windows Media (WMV)

Le paramètre *sourceURL* ne prend pas en charge les chaînes encodées en Unicode. Il doit pointer vers un contenu valide. Les redirections ne sont pas prises en charge.

Lorsque vous utilisez Windows XP, les fichiers audio sont automatiquement placés dans mes sous-dossiers de **musique** appropriés en fonction des valeurs de métadonnées au niveau du fichier. Les fichiers vidéo sont placés dans \\ \\ \\ le type de *nombre aléatoire* à télécharger musique \\ , où *nombre aléatoire* est une valeur aléatoire générée par le lecteur Windows Media pour chaque utilisateur, et le *type* est soit « temps réel », soit « arrière-plan », selon le type de téléchargement.

Lorsque vous utilisez le lecteur Windows Media série 9 avec Windows 98 et Windows Millennium Edition (me), les fichiers audio et vidéo sont placés dans \\ \\ \\  \\ le *type* de nombre aléatoire de musique Download, où le *nombre aléatoire* est une valeur aléatoire générée par le joueur pour chaque utilisateur, et le *type* est « temps réel » ou « arrière-plan », selon le type de téléchargement.

Notez que les fichiers peuvent être renommés en fonction des attributs de métadonnées contenus dans le fichier et des règles spécifiés par l’utilisateur dans la boîte de dialogue **options** . Les fichiers qui ne contiennent pas de métadonnées, tels que des **albums** ou des **artistes**, peuvent être déplacés vers des dossiers intitulés artiste inconnu ou album inconnu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DownloadCollection**](downloadcollection-object.md)
</dt> <dt>

[**Objet DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 






---
description: Les méthodes utilisées pour travailler avec des fichiers DirectX. x peuvent retourner les valeurs suivantes en plus des valeurs de retour COM standard. Action déconseillée.
ms.assetid: a91168bc-966a-47b5-ba83-fc480593228d
title: Valeurs de retour (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Return
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 7d465b9759d958cba06bf0b950bc67772fbb84a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516865"
---
# <a name="return-values-dxfileh"></a>Valeurs de retour (DXFile. h)

Les méthodes utilisées pour travailler avec des fichiers DirectX. x peuvent retourner les valeurs suivantes en plus des valeurs de retour COM standard. Action déconseillée.

<dl> <dt>

<span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE \_ OK**
</dt> <dd>

Command completed successfully.

</dd> <dt>

<span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR \_ BADALLOC**
</dt> <dd>

L'allocation de mémoire a échoué.

</dd> <dt>

<span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR \_ BADARRAYSIZE**
</dt> <dd>

La taille du tableau n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR \_ BADCACHEFILE**
</dt> <dd>

Le fichier cache contenant la date du fichier. x n’est pas valide. Un fichier cache contient les données extraites du réseau, mises en cache sur le disque dur et récupérées dans les demandes suivantes.

</dd> <dt>

<span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR \_ BADDataReference**
</dt> <dd>

La référence de données n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR \_ BadFile**
</dt> <dd>

Le fichier n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR \_ BADFILECOMPRESSIONTYPE**
</dt> <dd>

Le type de compression de fichier n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR \_ BADFILEFLOATSIZE**
</dt> <dd>

La taille à virgule flottante n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR \_ BADFILETYPE**
</dt> <dd>

Le fichier n’est pas un fichier DirectX. x.

</dd> <dt>

<span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR \_ BADFILEVERSION**
</dt> <dd>

La version du fichier n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR \_ BADINTRINSICS**
</dt> <dd>

Les intrinsèques ne sont pas valides.

</dd> <dt>

<span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR \_ BADOBJECT**
</dt> <dd>

L'objet n'est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR \_ BADRESOURCE**
</dt> <dd>

La ressource n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR \_ BADSTREAMHANDLE**
</dt> <dd>

Le descripteur de flux n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR \_ BADTYPE**
</dt> <dd>

Le type d’objet n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR \_ BADVALUE**
</dt> <dd>

Le paramètre n’est pas valide.

</dd> <dt>

<span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR \_ FILENOTFOUND**
</dt> <dd>

Fichier introuvable.

</dd> <dt>

<span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR \_ INTERNALERROR**
</dt> <dd>

Une erreur interne s’est produite.

</dd> <dt>

<span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR \_ NOinternet**
</dt> <dd>

Connexion Internet introuvable.

</dd> <dt>

<span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR \_ NOMOREDATA**
</dt> <dd>

Aucune autre donnée n’est disponible.

</dd> <dt>

<span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR \_ NOMOREOBJECTS**
</dt> <dd>

Tous les objets ont été énumérés.

</dd> <dt>

<span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR \_ NOMORESTREAMHANDLES**
</dt> <dd>

Aucun handle de flux n’est disponible.

</dd> <dt>

<span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR \_ NOTDONEYET**
</dt> <dd>

L’opération n’est pas terminée.

</dd> <dt>

<span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR \_ NotFound**
</dt> <dd>

Objet introuvable.

</dd> <dt>

<span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR \_ PARSEERROR**
</dt> <dd>

Impossible d’analyser le fichier.

</dd> <dt>

<span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR \_ RESOURCENOTFOUND**
</dt> <dd>

Ressource introuvable.

</dd> <dt>

<span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR \_ NOtemplate**
</dt> <dd>

Aucun modèle disponible.

</dd> <dt>

<span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR \_ URLNOTFOUND**
</dt> <dd>

URL introuvable.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DXFile. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence de fichier X (héritée)](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 





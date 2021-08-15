---
description: Spécifie une liste de commandes de script et les paramètres d’un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de commande de script dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: Attribut MF_PD_ASF_SCRIPT (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b98a078b0196add597ab184703306a7b2eba260082e3544ae84697b70bf71822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740720"
---
# <a name="mf_pd_asf_script-attribute"></a>\_Attribut de script MF PD \_ ASF \_

Spécifie une liste de commandes de script et les paramètres d’un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de commande de script dans l’en-tête ASF, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’en-tête de l’objet de commande de script. Le tableau suivant indique le format de l’objet BLOB :



| Champ de l’objet de commande de script | Type de données    | Taille    | Description               |
|-----------------------------|--------------|---------|---------------------------|
| Nombre de commandes              | **DWORD**    | 4 octets | Nombre de commandes de script |
| Type de commande, commandes      | **POIDS**\[\] | Variable  | Tableau de commandes de script  |



 

Le premier **DWORD** est le nombre de commandes de script, suivi d’un tableau de commandes. Chaque commande de script a le format suivant :



| Champ de l’objet de commande de script | Type de données     | Taille    | Description                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| Longueur du nom de la commande         | **DWORD**     | 4 octets | Taille de la chaîne de commande en octets, y compris le caractère NULL.      |
| Nom de la commande                | **WCHAR**\[\] | Variable  | Chaîne terminée par le caractère null qui contient la commande de script.                 |
| Longueur du nom du type de commande    | **DWORD**     | 4 octets | Taille de la chaîne de type de commande, en octets, y compris le caractère NULL. |
| Nom du type de commande           | **WCHAR**\[\] | Variable  | Chaîne terminée par le caractère null qui contient le type de commande.                   |
| Heure de présentation           | **DWORD**     | 4 octets | Durée de présentation de la commande, en millisecondes.                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> </dl>

 

 





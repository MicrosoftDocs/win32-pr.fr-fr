---
description: Contient le chemin d’accès du fichier d’icône pour la connexion.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Élément ICONFilePath (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519520"
---
# <a name="iconfilepath-mbnprofile-element"></a>Élément ICONFilePath (MBNProfile)

L’élément **ICONFilePath (MBNProfile)** contient le chemin d’accès du fichier d’icône pour la connexion.

L’interface utilisateur de connexion du système d’exploitation affiche cette icône lorsqu’une connexion est établie à l’aide de cet élément.

Lorsque vous passez le XML pour créer le profil dans la méthode [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) de l’interface [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) , ce chemin d’accès doit pointer vers l’emplacement source du fichier d’icône. En cas de réussite de la création de l’objet [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) , le service haut débit mobile copie le fichier d’icône dans son magasin interne et le chemin du profil est modifié pour en tenir compte.

Le fichier d’icône doit être au format .bmp avec une dimension de pixel 32X32.

Cet élément est une chaîne d’une longueur maximale de 1024 caractères, contenant un chemin d’accès absolu au fichier.

L’élément est facultatif.

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

L’élément **ICONFilePath** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 





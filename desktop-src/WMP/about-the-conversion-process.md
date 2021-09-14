---
title: À propos du processus de conversion
description: À propos du processus de conversion
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Lecteur Windows Media, processus de conversion
- plug-ins Lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232907"
---
# <a name="about-the-conversion-process"></a>À propos du processus de conversion

une fois que Lecteur Windows Media a instancié le plug-in de conversion, le processus se déroule comme suit :

1.  Le lecteur appelle [IWMPConvert :: convertfile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).
2.  Le plug-in convertit le fichier fourni dans le paramètre *bstrInputFile* au format ASF.
3.  Si la conversion échoue pour une raison quelconque, le plug-in retourne un code d’erreur approprié et le processus s’arrête.
4.  Si la conversion réussit, le plug-in place le fichier converti dans le dossier fourni dans le paramètre *bstrDestinationFolder* et retourne le chemin d’accès complet au fichier converti via le paramètre *pbstrOutputFile* .
5.  Le plug-in retourne un code de réussite de **convertfile**.
6.  Le lecteur copie le fichier converti dans un dossier dans la hiérarchie des dossiers musicaux de l’utilisateur. L’emplacement exact où le lecteur copie le fichier dépend du contenu. Dans le cadre de ce processus, le lecteur peut renommer le fichier.
7.  Le lecteur copie le fichier d’origine (non converti) dans un dossier de la hiérarchie des dossiers musicaux de l’utilisateur. Dans le cadre de ce processus, le lecteur peut renommer le fichier. Il s’agit de la copie du fichier que le lecteur utilise lorsque l’utilisateur synchronise le contenu de l’ordinateur sur un appareil qui requiert le format de fichier d’origine. Ce fichier s’appelle un *fichier caché*.
8.  Le lecteur ajoute à la bibliothèque des informations sur le fichier converti. Cela comprend la définition de la valeur de l’attribut **ShadowFilePath** sur le nouvel emplacement d’enregistrement du fichier caché.

Si vous devez utiliser le fichier converti, vous pouvez interroger la bibliothèque pour récupérer le contenu à l’aide des attributs **ContentDistributor** et **WM/UniqueFileIdentifier** . Si vous devez utiliser le fichier caché, vous devez tout de même récupérer l’objet **multimédia** du fichier converti, puis interroger l’attribut **ShadowFilePath** . Consultez [Ajout de métadonnées aux fichiers convertis](adding-metadata-to-converted-files.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des plug-ins de conversion**](about-conversion-plug-ins.md)
</dt> <dt>

[**Ajout de métadonnées aux fichiers convertis**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Lecture des valeurs d’attribut**](reading-attribute-values.md)
</dt> <dt>

[**Attribut ShadowFilePath**](shadowfilepath-attribute.md)
</dt> <dt>

[**Attribut WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Attribut WM/UniqueFileIdentifier**](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 





---
title: Pour modifier des métadonnées avec le writer
description: Pour modifier des métadonnées avec le writer
ms.assetid: 86badfe3-64bc-4285-a231-f6c0ebf4f262
keywords:
- Windows Media Format SDK, modification des métadonnées avec le writer
- Windows Media Format SDK, modification des métadonnées
- ASF (Advanced Systems Format), modification des métadonnées avec l’enregistreur
- ASF (format de systèmes avancés), modification des métadonnées avec le writer
- ASF (Advanced Systems Format), modification des métadonnées
- ASF (format de systèmes avancés), modification de métadonnées
- métadonnées, modification avec l’enregistreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2823b266b51da366683ac0b5cf65e10debf1ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523965"
---
# <a name="to-edit-metadata-with-the-writer"></a>Pour modifier des métadonnées avec le writer

Vous pouvez accéder, directement à partir de l’enregistreur, aux métadonnées qui seront placées dans l’en-tête du fichier. Appelez la méthode **QueryInterface** de toute interface dans l’objet Writer pour obtenir un pointeur vers l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) . Une fois que vous avez un pointeur vers l’interface appropriée, vous pouvez manipuler les métadonnées comme vous le feriez si vous aviez chargé le fichier dans l’objet de l’éditeur de métadonnées. Pour plus d’informations sur la modification des métadonnées, consultez [utilisation des métadonnées](working-with-metadata.md).

Vous devez apporter toutes les modifications aux métadonnées avant d’appeler [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

> [!Note]  
> Si vous définissez des métadonnées pour un fichier, écrivez le fichier, puis préparez l’écriture d’un nouveau fichier sans libérer l’enregistreur, certaines métadonnées qui ont été définies pour le premier fichier resteront définies et seront incluses dans les fichiers suivants. Lors de l’écriture de plusieurs fichiers avec la même instance de l’objet Writer, vous avez deux options : vérifier toutes les métadonnées avant d’écrire chaque fichier, ou uniquement écrire dans les métadonnées du writer qui s’appliquent à tous les fichiers que vous écrivez.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 





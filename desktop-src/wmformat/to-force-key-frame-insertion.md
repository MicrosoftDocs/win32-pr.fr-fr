---
title: Pour forcer l’insertion d' Key-Frame
description: Pour forcer l’insertion d' Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- ASF (Advanced Systems Format), forçage des insertions de trame clé
- ASF (format de systèmes avancés), forcer les insertions de trame clé
- ASF (Advanced Systems Format), insertions d’image clé
- ASF (format des systèmes avancés), insertions d’image clé
- images clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d400c0ee4ba97aa7de559b1394dbe5c9fb2a974c124924aeae0839b1b4dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196495"
---
# <a name="to-force-key-frame-insertion"></a>Pour forcer l’insertion d' Key-Frame

le codec Windows Media Video 9 prend en charge l’insertion d’image clé forcée. Lorsque vous transmettez un exemple au writer, vous pouvez spécifier qu’il doit être encodé sous la forme d’une [*image clé*](wmformat-glossary.md).

Pour forcer l’insertion d’une image clé pour un exemple, procédez comme suit.

1.  Allouez une mémoire tampon pour contenir l’exemple et récupérez un pointeur vers l’interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) contenant la mémoire tampon en appelant [**IWMWriter :: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Récupérez l’emplacement et la taille de la mémoire tampon créée à l’étape 1 en appelant [**INSSBuffer :: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).
3.  Copiez vos données d’exemple dans l’emplacement de la mémoire tampon, en vous assurant que l’exemple passé sera contenu dans la mémoire tampon allouée. En fonction de la source de vos exemples, vous pouvez utiliser diverses fonctions pour copier les données. Par exemple, si vous copiez un flux à partir d’un fichier AVI, vous pouvez utiliser la fonction AVI, **AVIStreamRead**.
4.  Mettez à jour la quantité de données utilisées dans la mémoire tampon pour refléter la taille réelle de l’exemple en appelant [**INSSBuffer :: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Obtenez un pointeur vers l’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) en appelant **INSSBuffer :: QueryInterface**.
6.  Définissez l’exemple comme une image clé forcée en appelant la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) pour définir la \_ propriété WM SampleExtensionGUID \_ OutputCleanPoint. Cette propriété est une valeur booléenne ; Affectez-lui la valeur **true**.
7.  Transmettez l’interface de mémoire tampon à l’enregistreur avec le nombre d’entrées et l’heure d’échantillonnage à l’aide de la méthode [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**Pour écrire des exemples**](to-write-samples.md)
</dt> <dt>

[**Encodage à vitesse de transmission variable (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 





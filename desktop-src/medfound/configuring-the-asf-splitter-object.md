---
description: Configuration de l’objet Splitter ASF
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Configuration de l’objet Splitter ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7068f2c869f6c73447b3341baee7221cdf8efbacec47ecdfa3a584bfb456f199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606149"
---
# <a name="configuring-the-asf-splitter-object"></a>Configuration de l’objet Splitter ASF

L’objet *séparateur* ASF est un objet de couche WMContainer qui analyse l’objet de données ASF d’un fichier ASF (Advanced Systems Format). Une fois le séparateur créé et initialisé pour analyser l’objet de données ASF d’un fichier multimédia, le séparateur doit être configuré pour générer des échantillons pour des flux spécifiques. Appelez [**IMFASFSplitter :: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) pour sélectionner les flux requis.

Éventuellement, une application peut également la configurer pour générer des échantillons dans l’ordre inverse ou générer des exemples pour le contenu protégé. Pour définir ces options, appelez [**IMFASFSplitter :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) et transmettez la combinaison d’opérations de bits requise des indicateurs pris en charge. Avant d’appeler cette méthode, le client doit terminer l’appel [**IMFASFSplitter :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) avec succès ; Sinon, **SetFlags** échoue avec le code **d’erreur MF \_ E \_ not \_ Initialized** . Pour plus d’informations sur l’initialisation du séparateur, consultez [création de l’objet séparateur ASF](creating-the-asf-splitter-object.md).

Pour vérifier si cet indicateur est actuellement défini sur le séparateur, appelez [**IMFASFSplitter :: GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags).

## <a name="selecting-streams-for-parsing"></a>sélection de Flux pour l’analyse

Pendant le processus d’initialisation via l’appel [**IMFASFSplitter :: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) , le séparateur détecte le nombre de flux et les identificateurs de flux dans le fichier ASF. Par défaut, aucun flux n’est sélectionné par le séparateur. L’application doit sélectionner les flux en appelant [**IMFASFSplitter :: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams). Cette méthode prend un tableau de nombres de flux. Pour obtenir le numéro de flux d’un flux, appelez [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) sur le profil ASF ou appelez [**IMFStreamDescriptor :: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) sur le descripteur de flux. (Vous pouvez obtenir le profil ASF et le descripteur de flux à partir de l’objet ContentInfo.) Si le client passe un numéro de flux qui n’est pas reconnu par le séparateur, il échoue avec une erreur **MF \_ E \_ INVALIDSTREAMNUMBER** .

L’appel de [**SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) efface les sélections précédentes. Tout flux qui n’est pas spécifié dans le tableau n’est pas sélectionné. Pour obtenir la liste des flux actuellement sélectionnés, appelez [**IMFASFSplitter :: GetSelectedStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams). Cette méthode prend un pointeur vers un tableau, que la méthode remplit avec les numéros de flux. Si la taille du tableau est inférieure au nombre de flux sélectionnés, la méthode échoue avec l’erreur **MF \_ E \_ BUFFERTOOSMALL** . Dans ce cas, la méthode retourne le nombre de flux sélectionnés dans le paramètre *pwNumStreams* . Vous pouvez ensuite utiliser ce nombre pour allouer un tableau de la taille correcte et appeler à nouveau la méthode.

Pour obtenir un exemple de code, consultez « sélectionner un flux pour l’analyse » dans le [Didacticiel : lecture d’un fichier ASF](tutorial--reading-an-asf-file.md).

## <a name="reverse-playback-setting"></a>Paramètre de lecture inversée

Pendant le processus d’initialisation du séparateur, il détermine si le contenu ASF prend en charge la lecture inversée. Si c’est le cas, le séparateur peut être configuré pour générer des échantillons dans l’ordre inverse, en définissant l’indicateur d' **\_ \_ annulation du séparateur MFASF** . Si le contenu ne prend pas en charge la lecture inversée, [**IMFASFSplitter :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) retourne **MF \_ E \_ INVALIDREQUEST**, mais l’indicateur est défini sur le séparateur.

Si le séparateur est configuré pour analyser dans le sens inverse, le séparateur commence toujours l’analyse à la fin de la mémoire tampon qui contient l’objet de données ASF. Par conséquent, pour l’analyse inverse, le décalage des données et la longueur des données à analyser doivent être définis correctement. Pour plus d’informations sur la définition des valeurs correctes, consultez [génération d’exemples de flux à partir d’un objet de données ASF existant](generating-stream-samples-from-an-existing-asf-data-object.md).

## <a name="protected-content-setting"></a>Paramètre de contenu protégé

Le séparateur peut être configuré pour utiliser le contenu de chiffrement au niveau du paquet en définissant le **\_ séparateur MFASF \_ WMDRM** via [**IMFASFSplitter :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags). cela indique au séparateur de fournir des exemples pour le contenu protégé par Windows Media Digital Rights Management (DRM). Lorsque cet indicateur est défini, les exemples générés par le séparateur contiennent les informations requises pour déchiffrer les données multimédia et reconstruire les frames, telles que l’attribut [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md) . Cet attribut est un objet BLOB qui contient un tableau de **DWORD** s. Chaque **DWORD** vous fournit les limites de charge utile pour le frame par rapport au début du frame. Si cet attribut n’est pas présent, le frame est contenu dans une seule charge utile. En règle générale, les exemples générés par le séparateur contiennent plusieurs mémoires tampons de média, l’application peut copier toutes les mémoires tampons dans une mémoire tampon contiguë en appelant [**IMFSample :: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). La mémoire tampon résultante contient le frame et la valeur de l’attribut contient des décalages dans cette mémoire tampon.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Séparateur ASF](asf-splitter.md)
</dt> </dl>

 

 




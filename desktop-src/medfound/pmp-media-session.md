---
description: Session média PMP
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: Session média PMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf2cb1ff173d6fd085f6e98dd4608c84ff40200
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092717"
---
# <a name="pmp-media-session"></a>Session média PMP

Une application peut créer la [session de média](media-session.md) dans un processus distinct appelé le processus PMP ( [protected Media Path](protected-media-path.md) ). L’objectif principal du processus PMP est d’activer la lecture de contenu protégé à l’aide de la gestion des droits numériques (DRM). Par défaut, le processus PMP est créé dans un environnement protégé (PE). Seuls les composants signés et approuvés peuvent être chargés dans un PE. L’un des avantages secondaires du processus PMP est qu’il isole le processus d’application du pipeline multimédia. Pour plus d’informations sur le processus PMP, consultez [chemin d’accès au média protégé](protected-media-path.md).

Pour créer la session multimédia à l’intérieur du processus PMP, appelez la fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) . Si vous le souhaitez, vous pouvez transmettre l’indicateur de **\_ \_ processus non protégé MFPMPSESSION** . Si cet indicateur est défini, le processus PMP est créé à l’intérieur d’un processus non protégé, et non d’un processus PE. Le processus non protégé ne peut pas être utilisé pour la lecture DRM, mais vous offre les avantages de l’isolation des processus.

La fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) retourne un pointeur vers un objet proxy pour la session multimédia. L’application communique avec la session multimédia par le biais du proxy.

![illustration de la session multimédia à l’intérieur du processus PMP](images/pmp01.png)

Par défaut, lorsque l’application crée une topologie, la source du média est créée à l’intérieur du processus d’application. Un proxy vers la source du média est créé à l’intérieur du processus PMP. La source du média peut créer des objets à l’intérieur du processus PMP à l’aide de l’interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) . Par exemple, pour prendre en charge la gestion des droits numériques (DRM), une source multimédia crée un objet appelé *autorité d’approbation d’entrée* (ITA). L’ITA doit être créé à l’intérieur du processus PMP. (Pour plus d’informations sur ITAs, consultez [chemin d’accès au média protégé](protected-media-path.md).) Pour utiliser l’interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , procédez comme suit :

1.  La source du média doit implémenter l’interface [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) .
2.  Pendant la résolution de la topologie, le proxy de session multimédia appelle la méthode [**IMFPMPClient :: SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) sur la source du média.
3.  La source multimédia appelle [**IMFPMPHost :: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) pour créer l’objet à l’intérieur du processus PMP. L’objet doit avoir un CLSID inscrit. En outre, pour charger dans le PE, l’objet doit être approuvé et signé numériquement. Pour plus d’informations sur la signature de code des composants multimédias protégés, consultez le livre blanc [Signing Code Signing for protected Media Components in Windows Vista (en](/windows-hardware/test/hlk/) anglais)

L’illustration suivante montre la source de média créée dans le processus d’application.

![illustration d’une source de média dans le processus d’application.](images/pmp02.png)

Une autre solution consiste à créer la source du média à l’intérieur de la session PMP.

1.  Définissez l' [**attribut \_ \_ \_ \_ mode Source distant de la session MF**](mf-session-remote-source-mode-attribute.md) lorsque vous créez la session multimédia. Les attributs de configuration sont spécifiés dans le paramètre *pConfiguration* de la fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .
2.  Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sur la session multimédia pour obtenir un pointeur vers l’interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) . L’identificateur de service est **MF \_ PMP \_ service**.
3.  Appelez [**IMFPMPHost :: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) avec l’identificateur de classe **CLSID \_ MFSourceResolver** pour créer le programme de résolution source à l’intérieur du processus PMP. La méthode retourne un pointeur vers un proxy pour le programme de résolution source.
4.  Appelez [**IMFSourceResolver :: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) ou [**IMFSourceResolver :: BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) pour créer la source du média.
    > [!Note]  
    > Dans ce cas, vous devez utiliser les versions asynchrones de ces méthodes, car les versions synchrones ne sont pas accessibles à distance.

     

L’illustration suivante montre la source de média créée dans le processus PMP.

![illustration d’une source de média dans le processus PMP.](images/pmp03.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment lire des fichiers multimédias protégés](how-to-play-protected-media-files.md)
</dt> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Chemin du média protégé](protected-media-path.md)
</dt> </dl>

 

 

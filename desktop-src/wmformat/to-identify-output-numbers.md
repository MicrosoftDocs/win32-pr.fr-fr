---
title: Pour identifier les numéros de sortie
description: Pour identifier les numéros de sortie
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media Format SDK, identification des numéros de sortie
- ASF (Advanced Systems Format), identification des numéros de sortie
- ASF (format de systèmes avancés), identification des numéros de sortie
- ASF (Advanced Systems Format), nombres et formats de sortie
- ASF (format des systèmes avancés), nombres et formats de sortie
- nombres et formats de sortie, identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c601481520632806ac56e12e16e1474336897d1be341c9d19df8e235d6355ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699379"
---
# <a name="to-identify-output-numbers"></a>Pour identifier les numéros de sortie

Pour identifier les numéros de sortie d’un fichier chargé, procédez comme suit. Ces procédures sont identiques pour le lecteur asynchrone et le lecteur synchrone. Lorsque les noms d’interface varient, les méthodes de lecture synchrone sont répertoriées entre parenthèses après les méthodes du lecteur asynchrone.

1.  Créez un objet lecteur et chargez un fichier pour la lecture. Pour plus d’informations, consultez [pour créer un lecteur et ouvrir un fichier](to-create-a-reader-and-open-a-file.md) (ou [pour créer un lecteur synchrone et ouvrir un fichier](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Récupérez le nombre total de sorties pour le fichier en appelant [**IWMReader :: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (ou [**IWMSyncReader :: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).
3.  Parcourez les sorties une par une, en effectuant les étapes suivantes pour chacune d’elles :
    -   Récupérez l’interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) pour la sortie actuelle avec un appel à [**IWMReader :: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (ou [**IWMSyncReader :: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).
    -   Récupérez la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour la sortie en effectuant deux appels à [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Effectuez le premier appel pour obtenir la taille de la structure, puis allouez de la mémoire pour celle-ci et transmettez un pointeur vers la mémoire allouée sur le deuxième appel. Vous pouvez également appeler [**IWMMediaProps :: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), qui fournit le type principal sans que vous ayez besoin d’allouer de la mémoire pour la structure du **\_ \_ type de média WM** . Vous pouvez ignorer les sorties d’un type majeur erroné.
    -   Récupérez le type de média et le sous-type de média principaux à partir de la structure du **\_ \_ type de média WM** . Ces valeurs sont stockées dans les membres de données **MajorType** et **SubType** respectivement.
    -   Vérifiez la valeur de **WM \_ Media \_ type. formatType**. Spécifie le type de structure contenu dans la mémoire tampon au niveau du **\_ type de média WM \_ . pbFormat**. Pour plus d’informations sur les types de format, consultez [types de médias](media-types.md).
    -   Allouez de la mémoire pour contenir la structure du type identifié à l’étape précédente. Copiez la structure dans votre mémoire allouée. Pour l’audio et la vidéo, cette structure vous donne des informations essentielles sur la façon dont les données doivent être rendues.

Le lecteur synchrone fournit également des méthodes pour récupérer des associations entre les numéros de sortie et les numéros de flux. Pour plus d’informations, consultez [pour rechercher des numéros de flux et des numéros de sortie](to-find-stream-numbers-and-output-numbers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**entrées, Flux et sorties**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Interface IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interface IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Utilisation des sorties**](working-with-outputs.md)
</dt> </dl>

 

 





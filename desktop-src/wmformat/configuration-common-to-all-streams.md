---
title: Configuration commune à tous les Flux
description: Configuration commune à tous les Flux
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- profils, configurations communes à tous les flux
- flux, configurations communes
- flux, noms
- flux, noms de connexion
- flux, nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522117"
---
# <a name="configuration-common-to-all-streams"></a>Configuration commune à tous les Flux

Tous les flux, quel que soit leur type, doivent recevoir un nom de flux, un nom de connexion et un numéro de flux.

Le nom du flux est simplement un nom descriptif que vous attribuez au flux. Un flux n’a pas besoin d’avoir un nom de flux, mais il vous aide à identifier le flux lorsque vous modifiez le profil ultérieurement. Vous pouvez définir un nom pour le flux en appelant [**IWMStreamConfig :: SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).

Chaque flux doit avoir un nom de connexion, également appelé nom d’entrée. Lorsque vous définissez le profil dans l’objet Writer pour écrire un fichier, le writer associe chaque nom de connexion à une entrée. Pour identifier les entrées, vous devez appeler [**IWMInputMediaProps :: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) pour récupérer le nom de la connexion. Les noms de connexion standard sont des descriptions simples du contenu, telles que « audio ». Si votre profil contient des flux qui sont mutuellement exclusifs par vitesse de transmission, chacun des flux mutuellement exclusifs doit avoir le même nom de connexion. Si ce n’est pas le cas, le profil n’est pas valide et sera rejeté par le writer. Vous pouvez définir un nom de connexion en appelant [**IWMStreamConfig :: SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).

Le numéro de flux identifie le flux au sein du fichier. Contrairement aux nombres d’entrée et aux numéros de sortie, les numéros de flux commencent à 1, et non à 0. Un numéro de flux est différent d’un index de flux, que vous utilisez pour obtenir des flux dans un profil à l’aide de [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream). L’index de flux est un nombre affecté au flux par l’objet de profil. Les index de flux sont compris entre 0 et un de moins que le nombre de flux récupérés par [**IWMProfile :: GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount). Les numéros de flux n’ont pas besoin d’être séquentiels, même s’ils sont généralement, et peuvent être compris entre 1 et 63. Vous pouvez définir un numéro de flux en appelant [**IWMStreamConfig :: SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de Flux**](configuring-streams.md)
</dt> <dt>

[**entrées, Flux et sorties**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 





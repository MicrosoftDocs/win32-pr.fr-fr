---
title: Utilisation de récepteurs personnalisés
description: Utilisation de récepteurs personnalisés
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- ASF (Advanced Systems Format), récepteurs personnalisés
- ASF (format des systèmes avancés), récepteurs personnalisés
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- récepteurs, récepteurs personnalisés
- récepteurs personnalisés, à propos de
- récepteurs d’écriture, récepteurs personnalisés
- récepteurs personnalisés, interface IWMWriterSink
- IWMWriterSink
- récepteurs d’écriture, interface IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293119"
---
# <a name="using-custom-sinks"></a>Utilisation de récepteurs personnalisés

Si vous avez besoin d’écriture spéciale, vous pouvez créer vos propres récepteurs de writer. L’enregistreur maintient une communication unidirectionnelle avec un récepteur en effectuant des appels aux méthodes de [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink). Pour créer votre propre récepteur, implémentez l’interface **IWMWriterSink** dans une classe de votre application. ce processus est très similaire à l’implémentation d’une autre interface de rappel utilisée par les objets du kit de développement logiciel (SDK) de Format multimédia Windows. Pour plus d’informations sur les rappels, consultez [utilisation des méthodes de rappel](using-the-callback-methods.md).

La mémoire tampon reçue dans [**IWMWriterSink :: OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) doit être écrite au début du fichier, et toutes les mémoires tampons reçues dans [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) doivent être écrites de manière séquentielle. **OnHeader** sera appelé au début, mais peut également être appelé à d’autres moments, et si c’est le cas, vous devriez, si possible, remplacer l’en-tête d’origine. Si votre application n’est pas en mesure de le faire pour une raison quelconque, ignorez simplement les appels **OnHeader** suivants.

Votre récepteur personnalisé doit communiquer son état à votre application d’écriture en effectuant des appels à la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Si vous implémentez votre récepteur en tant qu’objet COM, vous souhaiterez peut-être exposer l’interface [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) . Toutefois, vous pouvez transmettre l’adresse du rappel **OnStatus** à votre récepteur et définir un contexte comme vous le souhaitez.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> </dl>

 

 





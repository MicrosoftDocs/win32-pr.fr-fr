---
title: Pour prendre en charge plusieurs langues
description: Pour prendre en charge plusieurs langues
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Media Format SDK, prenant en charge plusieurs langues
- Windows Media Format SDK, prise en charge de plusieurs langues
- Windows Media Format SDK, prise en charge linguistique
- ASF (Advanced Systems Format), prenant en charge plusieurs langues
- ASF (format de systèmes avancés), prenant en charge plusieurs langues
- ASF (Advanced Systems Format), prise en charge de plusieurs langues
- ASF (Advanced Systems Format), prise en charge de plusieurs langues
- ASF (Advanced Systems Format), prise en charge des langues
- ASF (format des systèmes avancés), prise en charge des langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195919"
---
# <a name="to-support-multiple-languages"></a>Pour prendre en charge plusieurs langues

Vous pouvez prendre en charge plusieurs langues dans les flux et dans les métadonnées. le cœur de la prise en charge de plusieurs langues dans Windows Media Format SDK est l’interface [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , qui gère une liste des langues prises en charge. La liste de langues donne à chaque langage pris en charge un index, qui est utilisé dans différents objets du kit de développement logiciel (SDK) lors du traitement de plusieurs langues.

La méthode [**IWMLanguageList :: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) ajoute une langue à la liste. Vous pouvez identifier les langues déjà présentes dans la liste en obtenant le nombre total de langues avec [**IWMLanguageList :: GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) , puis en parcourant les langages appelant [**IWMLanguageList :: GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) pour chaque. L’index de langue est basé sur zéro.

## <a name="to-configure-mutual-exclusion-by-language"></a>Pour configurer l’exclusion mutuelle par langue

La configuration d’un objet d’exclusion mutuelle simple par langue est très simple. Chaque flux est maintenant associé à une langue. Le langage associé à un flux peut être défini à l’aide de [**IWMStreamConfig3 :: SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage). Une fois que tous les flux mutuellement exclusifs sont configurés, créez simplement un objet d’exclusion mutuelle comme vous le feriez pour tout autre type. Appelez ensuite [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) en passant \_ \_ le langage WMMUTEX CLSID pour le type.

les Flux qui s’excluent mutuellement par langue deviennent plus compliquées lorsque les flux exclusifs sont également mutuellement exclusifs par vitesse de transmission. Dans ce cas, vous devez utiliser des enregistrements qui s’excluent mutuellement, en procédant comme suit :

1.  Créez un objet d’exclusion mutuelle pour les flux de différents débits binaires dans chaque langue. Pour plus d’informations sur la création d’un objet d’exclusion mutuelle par vitesse de transmission, consultez [utilisation de l’exclusion mutuelle à vitesse de transmission multiple](using-multiple-bit-rate-mutual-exclusion.md).
2.  Créez un objet d’exclusion mutuelle. Appelez [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) et transmettez \_ le \_ langage WMMUTEX CLSID pour spécifier l’exclusivité par langue.
3.  Obtenez un pointeur vers l’interface [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) de l’objet exclusion mutuelle créé à l’étape 2 en appelant la méthode **QueryInterface** de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).
4.  Appelez la méthode [**IWMMutualExclusion2 :: AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) une fois pour chaque langage pour créer des enregistrements de flux qui s’excluent mutuellement.
5.  Pour chaque enregistrement créé à l’étape 4, ajoutez les flux de la langue appropriée avec les appels à [**IWMMutualExclusion2 :: AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).

## <a name="to-read-files-with-multiple-languages"></a>Pour lire des fichiers avec plusieurs langues

L’objet Reader fournit des méthodes permettant d’identifier les langages de flux disponibles dans un fichier. Vous pouvez récupérer le nombre de langues prises en charge pour une sortie en appelant [**IWMReaderAdvanced4 :: GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount). Vous pouvez ensuite récupérer des détails sur chaque langue avec des appels à [**IWMReaderAdvanced4 :: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).

Vous pouvez spécifier le langage à lire en passant l’index de cette langue au lecteur avec un appel à [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting). Cela permet de sélectionner la langue spécifiée tout en conservant la sélection de flux automatique pour tous les autres objets d’exclusion mutuelle dans le fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Rubriques avancées**](advanced-topics.md)
</dt> <dt>

[**Interface IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**Interface IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interface IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interface IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**Interface IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 





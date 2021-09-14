---
description: les tableaux suivants répertorient les clsid pour les catégories de filtre DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtrer les catégories
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e8c2b5e5f9e477633774cb24e707aa9d71060
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224420"
---
# <a name="filter-categories"></a>Filtrer les catégories

les tableaux suivants répertorient les clsid pour les catégories de filtre DirectShow.

-   [DirectShow Filtrer les catégories](#directshow-filter-categories)
-   [Autres catégories de filtres](#other-filter-categories)
-   [DirectShow Filtrer la méta-catégorie](#directshow-filter-meta-category)
-   [DMO Catégories](#dmo-categories)
-   [Rubriques connexes](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow Filtrer les catégories

Les catégories répertoriées ici sont énumérées par le [Mappeur de filtre](filter-mapper.md). Toutefois, par défaut, le mappeur de filtre ignore les catégories dont les mérites de mérite \_ n' \_ \_ utilisent pas ou moins. Pour plus d’informations, consultez [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Toutes les catégories répertoriées ici peuvent également être énumérées avec l' [énumérateur de périphérique système](system-device-enumerator.md).

Les catégories suivantes sont déclarées dans UUID. h. Incluez le fichier d’en-tête DShow. h.




| Nom convivial | CLSID | Mérite | 
|---------------|-------|-------|
| Sources de capture audio | <strong>CLSID_AudioInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Compresseurs audio | <strong>CLSID_AudioCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Convertisseurs audio | <strong>CLSID_AudioRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Filtres de contrôle de périphérique | <strong>CLSID_DeviceControlCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| DirectShow Filtres | <strong>CLSID_LegacyAmFilterCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Convertisseurs externes | <strong>CLSID_TransmitCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Convertisseurs midi | <strong>CLSID_MidiRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Sources de capture vidéo | <strong>CLSID_VideoInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Compresseurs vidéo | <strong>CLSID_VideoCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Périphériques de décompression de flux WDM | <strong>CLSID_DVDHWDecodersCategory</strong><blockquote>[!Note]<br />Cette catégorie contient les décodeurs de DVD matériels.</blockquote><br /> | <strong>MERIT_DO_NOT_USE</strong> | 
| Périphériques de capture de streaming WDM | <strong>AM_KSCATEGORY_CAPTURE</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Périphériques de distributeur de streaming WDM | <strong>AM_KSCATEGORY_CROSSBAR</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Périphériques de rendu de streaming WDM | <strong>AM_KSCATEGORY_RENDER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Périphériques de streaming WDM/Splitter | <strong>AM_KSCATEGORY_SPLITTER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Périphériques audio de diffusion en continu WDM | <strong>AM_KSCATEGORY_TVAUDIO</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Périphériques Tuner TV WDM streaming | <strong>AM_KSCATEGORY_TVTUNER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Codecs VBI de streaming WDM | <strong>AM_KSCATEGORY_VBICODEC</strong> | <strong>MERIT_DO_NOT_USE</strong> | 




 

Les catégories suivantes sont déclarées dans le fichier d’en-tête KS. h.



| Nom convivial                          | CLSID                                   | Mérite                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Transformations de communication de streaming WDM | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **MÉRITE \_ n' \_ \_ utilise pas** |
| Transformations de données de streaming WDM          | **KSCATEGORY \_ DATATRANSFORM**           | **MÉRITE \_ n' \_ \_ utilise pas** |
| Transformations de l’interface de streaming WDM     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **MÉRITE \_ n' \_ \_ utilise pas** |
| périphériques de Mixer de Streaming WDM            | **\_mélangeur KSCATEGORY**                   | **MÉRITE \_ n' \_ \_ utilise pas** |



 

Les catégories suivantes sont déclarées dans le fichier d’en-tête Bdamedia. h. Incluez les fichiers d’en-tête suivants : KS. h, ksmedia. h et bdamedia. h.



| Nom convivial                       | CLSID                                       | Mérite                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Fournisseurs de réseau BDA               | **\_fournisseur de \_ réseau KSCATEGORY BDA \_**      | **MÉRITE \_ normal**       |
| Composants du récepteur BDA             | **\_ \_ composant récepteur KSCATEGORY \_ BDA**    | **MÉRITE \_ n' \_ \_ utilise pas** |
| Filtres de rendu BDA               | **\_récepteur IP \_ KSCATEGORY**                    | **MÉRITE \_ n' \_ \_ utilise pas** |
| Filtres sources BDA                  | **\_ \_ tuner réseau KSCATEGORY \_ BDA**         | **MÉRITE \_ n' \_ \_ utilise pas** |
| Convertisseurs d’informations de transport BDA | **\_ \_ informations sur le transport BDA KSCATEGORY \_** | **MÉRITE \_ normal**       |



 

> [!Note]  
> les décodeurs sont inscrits sous la catégorie « filtres de DirectShow » (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Autres catégories de filtres

Les catégories répertoriées ici peuvent être énumérées avec l’énumérateur de périphérique système, mais ne sont pas visibles par le mappeur de filtre et ne sont pas utilisées par les [connecter intelligentes](intelligent-connect.md).

Les catégories suivantes sont déclarées dans le fichier d’en-tête qedit. h.



| Nom convivial            | Call                             | Mérite                   |
|--------------------------|----------------------------------|-------------------------|
| Effets vidéo (1 entrée)  | **CLSID \_ VideoEffects1Category** | **MÉRITE \_ n' \_ \_ utilise pas** |
| Effets vidéo (2 entrées) | **CLSID \_ VideoEffects2Category** | **MÉRITE \_ n' \_ \_ utilise pas** |



 

ces catégories contiennent des effets vidéo et des transitions pour les [Services d’édition DirectShow](directshow-editing-services.md):

-   « Effets vidéo (1 entrée) » contient des effets vidéo.
-   « Effets vidéo (2 entrées) » contient des transitions vidéo.

Pour plus d’informations, consultez [énumération des effets et des transitions](enumerating-effects-and-transitions.md).

Les catégories suivantes sont déclarées dans le fichier d’en-tête UUID. h. Incluez le fichier d’en-tête DShow. h.



| Nom convivial       | Call                                | Mérite                   |
|---------------------|-------------------------------------|-------------------------|
| Encodeurs encodeurs     | **CLSID \_ MediaEncoderCategory**     | **MÉRITE \_ n' \_ \_ utilise pas** |
| Multiplexeurs encapis | **CLSID \_ MediaMultiplexerCategory** | **MÉRITE \_ n' \_ \_ utilise pas** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow Filtre Meta-Category



| Nom convivial                 | CLSID                            | Mérite          |
|-------------------------------|----------------------------------|----------------|
| Catégories de filtre ActiveMovie | **CLSID \_ ActiveMovieCategories** | Non applicable |



 

Cette catégorie méta contient une liste de catégories de filtres. Si une catégorie de filtre n’apparaît pas dans cette liste, le [Mappeur de filtre](filter-mapper.md) ignore la catégorie, ce qui signifie que le filtre n’est pas disponible pour les [connecter intelligentes](intelligent-connect.md).

Pour énumérer la liste des catégories de filtre, appelez [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec la valeur CLSID \_ ActiveMovieCategories. Les monikers retournés par cette méthode prennent en charge les propriétés suivantes.



| Nom de la propriété  | Description                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| Convivial | Nom de la catégorie (VT \_ BSTR).                                                              |
| Mérite        | Mérite de catégorie (VT \_ I4). Si cette propriété est absente, Treat comme **mérite \_ n' \_ \_ utilise pas**. |
| IDENTIFICATEUR        | CLSID de catégorie (VT \_ BSTR).                                                             |



 

Pour ajouter une nouvelle catégorie de filtre à cette liste, appelez [**IFilterMapper2 :: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>DMO Catégories

les objets DMOs (DirectX Media objects) utilisent un mécanisme d’énumération différent de DirectShow filtres. Pour plus d’informations, consultez [inscription d’un DMO](registering-a-dmo.md). toutefois, vous pouvez utiliser l’énumérateur de périphérique système pour énumérer les catégories de DMO. les monikers sont liés au [filtre de Wrapper DMO](dmo-wrapper-filter.md) et initialisent automatiquement le filtre avec l’DMO.

en outre, certaines des catégories de DMO sont mappées à des catégories de filtre DirectShow à des fins de connexion intelligente :



| DMO Catégorie                    | DirectShow Identique              |
|---------------------------------|------------------------------------|
| **\_encodeur audio DMOCATEGORY \_** | **CLSID \_ AudioCompressorCategory** |
| **\_DÉcodeur audio DMOCATEGORY \_** | **CLSID \_ LegacyAmFilterCategory**  |
| **\_encodeur vidéo DMOCATEGORY \_** | **CLSID \_ VideoCompressorCategory** |
| **\_DÉcodeur vidéo DMOCATEGORY \_** | **CLSID \_ LegacyAmFilterCategory**  |



 

notez que les catégories effet vidéo et effet audio ne sont mappées à aucune catégorie de DirectShow.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes et GUID](constants-and-guids.md)
</dt> <dt>

[Énumération des appareils et des filtres](enumerating-devices-and-filters.md)
</dt> <dt>

[Connecter intelligente](intelligent-connect.md)
</dt> <dt>

[Disposition des clés de Registre](layout-of-the-registry-keys.md)
</dt> <dt>

[Utilisation du mappeur de filtre](using-the-filter-mapper.md)
</dt> <dt>

[Utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md)
</dt> </dl>

 

 





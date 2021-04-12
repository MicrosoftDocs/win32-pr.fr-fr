---
description: Les tableaux suivants répertorient les CLSID pour les catégories de filtre DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtrer les catégories
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385568"
---
# <a name="filter-categories"></a>Filtrer les catégories

Les tableaux suivants répertorient les CLSID pour les catégories de filtre DirectShow.

-   [Catégories de filtre DirectShow](#directshow-filter-categories)
-   [Autres catégories de filtres](#other-filter-categories)
-   [Méta-catégorie de filtre DirectShow](#directshow-filter-meta-category)
-   [Catégories DMO](#dmo-categories)
-   [Rubriques connexes](#related-topics)

## <a name="directshow-filter-categories"></a>Catégories de filtre DirectShow

Les catégories répertoriées ici sont énumérées par le [Mappeur de filtre](filter-mapper.md). Toutefois, par défaut, le mappeur de filtre ignore les catégories dont les mérites de mérite \_ n' \_ \_ utilisent pas ou moins. Pour plus d’informations, consultez [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Toutes les catégories répertoriées ici peuvent également être énumérées avec l' [énumérateur de périphérique système](system-device-enumerator.md).

Les catégories suivantes sont déclarées dans UUID. h. Incluez le fichier d’en-tête DShow. h.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom convivial</th>
<th>CLSID</th>
<th>Mérite</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sources de capture audio</td>
<td><strong>CLSID_AudioInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Compresseurs audio</td>
<td><strong>CLSID_AudioCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Convertisseurs audio</td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Filtres de contrôle de périphérique</td>
<td><strong>CLSID_DeviceControlCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Filtres DirectShow</td>
<td><strong>CLSID_LegacyAmFilterCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Convertisseurs externes</td>
<td><strong>CLSID_TransmitCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Convertisseurs midi</td>
<td><strong>CLSID_MidiRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Sources de capture vidéo</td>
<td><strong>CLSID_VideoInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Compresseurs vidéo</td>
<td><strong>CLSID_VideoCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Périphériques de décompression de flux WDM</td>
<td><strong>CLSID_DVDHWDecodersCategory</strong>
<blockquote>
[!Note]<br />
Cette catégorie contient les décodeurs de DVD matériels.
</blockquote>
<br/></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Périphériques de capture de streaming WDM</td>
<td><strong>AM_KSCATEGORY_CAPTURE</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Périphériques de distributeur de streaming WDM</td>
<td><strong>AM_KSCATEGORY_CROSSBAR</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Périphériques de rendu de streaming WDM</td>
<td><strong>AM_KSCATEGORY_RENDER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Périphériques de streaming WDM/Splitter</td>
<td><strong>AM_KSCATEGORY_SPLITTER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Périphériques audio de diffusion en continu WDM</td>
<td><strong>AM_KSCATEGORY_TVAUDIO</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Périphériques Tuner TV WDM streaming</td>
<td><strong>AM_KSCATEGORY_TVTUNER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Codecs VBI de streaming WDM</td>
<td><strong>AM_KSCATEGORY_VBICODEC</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
</tbody>
</table>



 

Les catégories suivantes sont déclarées dans le fichier d’en-tête KS. h.



| Nom convivial                          | CLSID                                   | Mérite                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Transformations de communication de streaming WDM | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **MÉRITE \_ n' \_ \_ utilise pas** |
| Transformations de données de streaming WDM          | **KSCATEGORY \_ DATATRANSFORM**           | **MÉRITE \_ n' \_ \_ utilise pas** |
| Transformations de l’interface de streaming WDM     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **MÉRITE \_ n' \_ \_ utilise pas** |
| Périphériques de mixage de streaming WDM            | **\_mélangeur KSCATEGORY**                   | **MÉRITE \_ n' \_ \_ utilise pas** |



 

Les catégories suivantes sont déclarées dans le fichier d’en-tête Bdamedia. h. Incluez les fichiers d’en-tête suivants : KS. h, ksmedia. h et bdamedia. h.



| Nom convivial                       | CLSID                                       | Mérite                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| Fournisseurs de réseau BDA               | **\_fournisseur de \_ réseau KSCATEGORY BDA \_**      | **MÉRITE \_ normal**       |
| Composants du récepteur BDA             | **\_ \_ composant récepteur KSCATEGORY \_ BDA**    | **MÉRITE \_ n' \_ \_ utilise pas** |
| Filtres de rendu BDA               | **\_récepteur IP \_ KSCATEGORY**                    | **MÉRITE \_ n' \_ \_ utilise pas** |
| Filtres sources BDA                  | **\_ \_ tuner réseau KSCATEGORY \_ BDA**         | **MÉRITE \_ n' \_ \_ utilise pas** |
| Convertisseurs d’informations de transport BDA | **\_ \_ informations sur le transport BDA KSCATEGORY \_** | **MÉRITE \_ normal**       |



 

> [!Note]  
> Les décodeurs sont inscrits sous la catégorie « filtres DirectShow » (CLSID \_ LegacyAmFilterCategory).

 

## <a name="other-filter-categories"></a>Autres catégories de filtres

Les catégories répertoriées ici peuvent être énumérées avec l’énumérateur de périphérique système, mais ne sont pas visibles par le mappeur de filtre et ne sont pas utilisées par la [connexion intelligente](intelligent-connect.md).

Les catégories suivantes sont déclarées dans le fichier d’en-tête qedit. h.



| Nom convivial            | Call                             | Mérite                   |
|--------------------------|----------------------------------|-------------------------|
| Effets vidéo (1 entrée)  | **CLSID \_ VideoEffects1Category** | **MÉRITE \_ n' \_ \_ utilise pas** |
| Effets vidéo (2 entrées) | **CLSID \_ VideoEffects2Category** | **MÉRITE \_ n' \_ \_ utilise pas** |



 

Ces catégories contiennent des effets vidéo et des transitions pour les [services de modification DirectShow](directshow-editing-services.md):

-   « Effets vidéo (1 entrée) » contient des effets vidéo.
-   « Effets vidéo (2 entrées) » contient des transitions vidéo.

Pour plus d’informations, consultez [énumération des effets et des transitions](enumerating-effects-and-transitions.md).

Les catégories suivantes sont déclarées dans le fichier d’en-tête UUID. h. Incluez le fichier d’en-tête DShow. h.



| Nom convivial       | Call                                | Mérite                   |
|---------------------|-------------------------------------|-------------------------|
| Encodeurs encodeurs     | **CLSID \_ MediaEncoderCategory**     | **MÉRITE \_ n' \_ \_ utilise pas** |
| Multiplexeurs encapis | **CLSID \_ MediaMultiplexerCategory** | **MÉRITE \_ n' \_ \_ utilise pas** |



 

## <a name="directshow-filter-meta-category"></a>Meta-Category de filtre DirectShow



| Nom convivial                 | CLSID                            | Mérite          |
|-------------------------------|----------------------------------|----------------|
| Catégories de filtre ActiveMovie | **CLSID \_ ActiveMovieCategories** | Non applicable |



 

Cette catégorie méta contient une liste de catégories de filtres. Si une catégorie de filtre n’apparaît pas dans cette liste, le [Mappeur de filtre](filter-mapper.md) ignore la catégorie, ce qui signifie que le filtre n’est pas disponible pour la [connexion intelligente](intelligent-connect.md).

Pour énumérer la liste des catégories de filtre, appelez [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec la valeur CLSID \_ ActiveMovieCategories. Les monikers retournés par cette méthode prennent en charge les propriétés suivantes.



| Nom de la propriété  | Description                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| Convivial | Nom de la catégorie (VT \_ BSTR).                                                              |
| Mérite        | Mérite de catégorie (VT \_ I4). Si cette propriété est absente, Treat comme **mérite \_ n' \_ \_ utilise pas**. |
| IDENTIFICATEUR        | CLSID de catégorie (VT \_ BSTR).                                                             |



 

Pour ajouter une nouvelle catégorie de filtre à cette liste, appelez [**IFilterMapper2 :: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>Catégories DMO

Les objets DMOs (DirectX Media Objects) utilisent un mécanisme d’énumération différent des filtres DirectShow. Pour plus d’informations, consultez [inscription d’un DMO](registering-a-dmo.md). Toutefois, vous pouvez utiliser l’énumérateur de périphérique système pour énumérer les catégories DMO. Les monikers sont liés au [filtre de wrappers DMO](dmo-wrapper-filter.md) et initialisent automatiquement le filtre avec DMO.

En outre, certaines des catégories DMO sont mappées à des catégories de filtre DirectShow dans le cadre de la connexion intelligente :



| Catégorie DMO                    | Équivalent DirectShow              |
|---------------------------------|------------------------------------|
| **\_encodeur audio DMOCATEGORY \_** | **CLSID \_ AudioCompressorCategory** |
| **\_DÉcodeur audio DMOCATEGORY \_** | **CLSID \_ LegacyAmFilterCategory**  |
| **\_encodeur vidéo DMOCATEGORY \_** | **CLSID \_ VideoCompressorCategory** |
| **\_DÉcodeur vidéo DMOCATEGORY \_** | **CLSID \_ LegacyAmFilterCategory**  |



 

Notez que les catégories effet vidéo et effet audio ne sont mappées à aucune catégorie DirectShow.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes et GUID](constants-and-guids.md)
</dt> <dt>

[Énumération des appareils et des filtres](enumerating-devices-and-filters.md)
</dt> <dt>

[Connexion intelligente](intelligent-connect.md)
</dt> <dt>

[Disposition des clés de Registre](layout-of-the-registry-keys.md)
</dt> <dt>

[Utilisation du mappeur de filtre](using-the-filter-mapper.md)
</dt> <dt>

[Utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md)
</dt> </dl>

 

 





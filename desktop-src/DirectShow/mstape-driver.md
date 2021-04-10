---
description: Pilote MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Pilote MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845754"
---
# <a name="mstape-driver"></a>Pilote MSTape

Cette rubrique s’applique à Windows XP ou version ultérieure.

Le pilote MSTape prend en charge les appareils caméscopes D-VHS et MPEG. Il est exposé aux applications en tant que filtre de [capture vidéo WDM](wdm-video-capture-filter.md) . Sa fonctionnalité est semblable à celle de [MSDV](msdv-driver.md), le pilote de caméscope DV :

-   Il apparaît dans les catégories de filtres « sources de capture vidéo » (CLSID \_ VideoInputDeviceCategory) et « périphériques de rendu de streaming WDM » (am \_ KSCATEGORY \_ Render).
-   Une application peut créer une instance du filtre à l’aide de l’interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .
-   Il possède une broche de sortie pour la capture et le transport à partir de l’appareil, et une broche d’entrée pour le transport vers l’appareil. Un seul code confidentiel peut être connecté à la fois.

**Types de médias**

La broche d’entrée prend en charge un type de média.



|              |                                                            |
|--------------|------------------------------------------------------------|
| Type principal   | Flux de MEDIATYPE \_                                          |
| Subtype      | \_Stride de \_ transport MEDIASUBTYPE MPEG2 \_                     |
| Taille d’échantillon  | 192 x 256                                                  |
| Bloc de format | [**\_Stride transport \_ MPEG2**](mpeg2-transport-stride.md) |



 

La broche de sortie prend en charge deux types de médias.



|              |                                        |
|--------------|----------------------------------------|
| Type principal   | Flux de MEDIATYPE \_                      |
| Subtype      | \_Stride de \_ transport MEDIASUBTYPE MPEG2 \_ |
| Taille d’échantillon  | 192 x 256                              |
| Bloc de format | \_Stride transport \_ MPEG2               |



 



|              |                                        |
|--------------|----------------------------------------|
| Type principal   | Flux de MEDIATYPE \_                      |
| Subtype      | \_Stride de \_ transport MEDIASUBTYPE MPEG2 \_ |
| Taille d’échantillon  | 188 x 256                              |
| Bloc de format | **NULL**                               |



 

**Informations sur l’appareil**

Le pilote lit dynamiquement les informations à partir de la ROM de configuration de l’appareil. L’application peut récupérer ces informations en liant le moniker de l’appareil à un jeu de propriétés et en appelant la méthode **IPropertyBag :: Read** .



| Propriété            | Description                                                                                                                                                                         | Type de données           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueId \_ faible       | ID unique de l’appareil ( **DWORD** faible).                                                                                                                                            | **long** (VT \_ I4)   |
| UniqueId \_ élevé      | ID unique de l’appareil ( **DWORD** haute)                                                                                                                                            | **long**            |
| VendorID            | ID du fournisseur.                                                                                                                                                                          | **long**            |
| ModelID             | ID du modèle                                                                                                                                                                           | **long**            |
| VendorText          | Nom du fournisseur.                                                                                                                                                                        | **BSTR** (VT \_ BSTR) |
| ModelText           | Nom du modèle d’appareil.                                                                                                                                                                  | **BSTR**            |
| UnitModelText       | Nom du modèle d’unité ; peut être identique à ModelText.                                                                                                                                      | **BSTR**            |
| DeviceOPcr0Payload  | charge utile oPCR (sortie de contrôle du plug-in). Exemple : 146 quadlets.                                                                                                                          | **long**            |
| DeviceOPcr0DataRate | débit de données oPCR. Exemples : 0 (S100), 1 (S200) ou 2 (s400).                                                                                                                          | **long**            |
| DeviceClassGUID     | GUID qui identifie le pilote de périphérique. Pour MSTape, cette valeur est `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` . Ce GUID est défini en tant que MSTapeDeviceGUID dans le fichier d’en-tête Xprtdefs. h. | **BSTR**            |
| Description         | Description de l’appareil, prise à partir du fichier INF. Cette chaîne contient généralement le nom de la personnalisation de l’appareil.                                                                    | **BSTR**            |



 

L’ID d’appareil est un entier 64 bits. La **valeur DWORD** basse est stockée dans la propriété Low UniqueId \_ , et la **valeur DWORD** High est stockée dans la propriété High UniqueId \_ .

Pour plus d’informations sur les monikers de périphérique, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




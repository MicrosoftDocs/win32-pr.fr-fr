---
description: Microsoft XPS Document Writer (MXDW) permet aux utilisateurs de créer des fichiers de document xps en imprimant à partir de n’importe quelle application Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Paramètres de Configuration MXDW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75d45ea3ad9c8c74280d1e70e418ee0bf4823d1f0332e3d5c772d29976cf2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971188"
---
# <a name="mxdw-configuration-settings"></a>Paramètres de Configuration MXDW

Microsoft XPS Document Writer (MXDW) permet aux utilisateurs de créer des fichiers de document xps en imprimant à partir de n’importe quelle application Windows. Les développeurs d’applications peuvent contrôler les paramètres de sortie suivants du MXDW à l’aide des parties PrintTicket et PrintCapabilities du [schéma d’impression](./printschema.md).

## <a name="jobinterleaving"></a>JobInterleaving

Le paramètre JobInterleaving contrôle l’ordre d’entrelacement du contenu pour les documents XPS. Pour plus d’informations sur l’entrelacement de travaux, consultez la [spécification Paper XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf). MXDW prend en charge les deux options suivantes pour ce paramètre :

-   **Off** : cette option désactive l’entrelacement afin que toutes les données de chaque élément de contenu dans le document soient contiguës, ce qui améliore l’efficacité de l’accès aléatoire. Cette option est idéale pour l’affichage d’un document XPS.
-   **On** : cette option permet l’entrelacement afin que les données de chaque élément de contenu soient réparties et réorganisées pour un traitement séquentiel plus efficace. Cette option est idéale pour le téléchargement et l’impression sur le Web.

L’exemple suivant est un exemple du code XML PrintCapabilities qui comprend le paramètre JobInterleaving.


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



Le code XML PrintTicket est similaire, à ceci près qu’il spécifie une option particulière. Pour plus d’informations, consultez le [schéma d’impression](./printschema.md) .

Étant donné que JobInterleaving n’est pas l’un des [Mots clés publics du schéma d’impression](./print-schema-public-keywords.md), vous devez inclure une déclaration de l’espace de noms (dans le cas présent « ns0000 » dans la balise **PrintCapabilities** (ou **PrintTicket**) au début du document PrintCapabilities (ou PrintTicket), comme indiqué dans l’exemple suivant :


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>JobImageType

JobImageType contrôle le format de sortie des formats bitmap incorporés. MXDW prend en charge les quatre options suivantes pour ce paramètre :

-   **JPEGHigh** : cette option spécifie l’image JPEG avec un haut niveau de compression. Cette option produit la plus petite taille de fichier, mais la qualité d’image la plus faible.
-   **JPEGMed** : cette option spécifie l’image JPEG avec un niveau de compression moyen. Cette option fournit le meilleur équilibre entre la taille de fichier et la qualité d’image.
-   **JPEGLow** : cette option spécifie l’image JPEG avec un niveau de compression faible. Cette option produit le moins de réduction de la taille des fichiers et de la qualité d’image élevée.
-   **Png** : cette option spécifie le format d’image png avec compression sans perte. Cette option produit la taille de fichier la plus grande et la qualité d’image la plus élevée.

Le code XML PrintCapabilities du paramètre JobImageType apparaît ci-dessous :


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



Le code XML PrintTicket est similaire, à ceci près qu’il spécifie une option particulière. Pour plus d’informations, consultez le [schéma d’impression](./printschema.md) .

Étant donné que JobImageType n’est pas l’un des [Mots clés publics du schéma d’impression](./print-schema-public-keywords.md), vous devez inclure une déclaration de l’espace de noms (dans le cas présent « ns0000 » dans la balise **PrintCapabilities** (ou **PrintTicket**) au début du document PrintCapabilities (ou PrintTicket), comme indiqué dans l’exemple suivant :


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Schéma d’impression](./printschema.md)
</dt> <dt>

[Spécifications XPS et téléchargements de licences](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

---
title: La structure FORMATETC
description: La structure FORMATETC est un format de presse-papiers généralisé, amélioré pour englober un appareil cible, un aspect ou une vue des données et un support de stockage.
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece0079cf2c0f07b7356f07ee2c53b1279b7ce7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221708"
---
# <a name="the-formatetc-structure"></a>La structure FORMATETC

La structure FORMATETC est un format de presse-papiers généralisé, amélioré pour englober un appareil cible, un *aspect* ou une vue des données et un support de stockage. Un consommateur de données, tel qu’une application de conteneur OLE, passe la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) en tant qu’argument dans les appels à [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) pour indiquer le type de données qu’il souhaite à partir d’une source de données, tel qu’un objet de document composé. La source utilise la structure **FORMATETC** pour décrire les formats qu’elle peut fournir.

[**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) peut décrire pratiquement toutes les données, y compris d’autres objets tels que les monikers. Un conteneur peut demander à l’un de ses objets incorporés de répertorier ses formats de données en appelant [**IDataObject :: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), qui retourne un objet énumérateur qui implémente l’interface [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) . Au lieu de répondre simplement à la présence de « texte et d’une image bitmap », l’objet peut fournir une description détaillée des données, y compris l’appareil (généralement l’écran ou l’imprimante) pour laquelle il est affiché, l’aspect à présenter à l’utilisateur (contenu complet, miniature, icône ou format pour l’impression) et le support de stockage contenant les données (mémoire globale,  fichier de disque, objet de stockage ou flux). Cette capacité à décrire de manière rigoureuse les données sera, dans le temps, aboutir à une meilleure qualité d’imprimante et de sortie d’écran, ainsi qu’une meilleure efficacité dans l’exploration des données, où une esquisse miniature est beaucoup plus rapide à récupérer et à afficher qu’un rendu entièrement détaillé.

Le tableau suivant répertorie les champs de la structure de données [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) et les informations qu’elles spécifient.



| Champ                   | Spécifie                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | Format dans lequel les données doivent être restituées, qui peut être un format de presse-papiers standard, un format propriétaire ou un format OLE. Pour plus d’informations sur les formats OLE, consultez [documents composés](compound-documents.md).<br/>                                          |
| **PTD**<br/>      | une structure [**DVTARGETDEVICE**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice) , qui contient suffisamment d’informations sur un Windows appareil cible, tel qu’un écran ou une imprimante, afin qu’un handle vers son contexte de périphérique (hDC) puisse être créé à l’aide de la fonction [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) . <br/> |
| **dwAspect**<br/> | Aspect ou vue des données à rendre ; peut être le contenu complet, une esquisse miniature, une icône ou un format pour l’impression.<br/>                                                                                                                                  |
| **lindex**<br/>   | Partie de l’aspect intéressant ; pour le présent, la valeur doit être-1, ce qui indique que l’intégralité de la vue est intéressante.<br/>                                                                                                                                |
| **TYMED**<br/>    | Le support de stockage des données, qui peut être une mémoire globale, un fichier de disque ou une instance de l’une des interfaces de stockage structuré de COM.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Formats de données et média de transfert](data-formats-and-transfer-media.md)
</dt> </dl>

 


---
title: WM/WMShadowFileSourceDRMType (kit de développement logiciel (SDK) Windows Media format 11)
description: L’attribut WM/WMShadowFileSourceDRMType contient le type de gestion des droits qui est utilisé pour protéger le fichier d’origine à partir duquel le fichier ASF est dérivé.
ms.assetid: 58e7a383-6e80-42fc-bc75-5920dbe67a40
keywords:
- Format Windows Media WM/WMShadowFileSourceDRMType
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceDRMType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f33d961e8cd3645e4949980d91fe4de79119f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032244"
---
# <a name="wmwmshadowfilesourcedrmtype-windows-media-format-11-sdk"></a>WM/WMShadowFileSourceDRMType (kit de développement logiciel (SDK) Windows Media format 11)

L’attribut **WM/WMShadowFileSourceDRMType** contient le type de gestion des droits qui est utilisé pour protéger le fichier d’origine à partir duquel le fichier ASF est dérivé.

## <a name="global-constant"></a>Constante globale

\_wszWMWMShadowFileSourceDRMType g

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Le contenu qui existe dans un format de fichier autre que ASF et qui est protégé par une certaine sorte de gestion des droits peut être converti en fichier Windows Media protégé par Windows Media DRM par le biais d’un processus appelé importation de licence. Ce fichier ASF doit contenir cet attribut, ainsi que WM/WMShadowFileSourceFileType pour suivre l’origine du contenu.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 





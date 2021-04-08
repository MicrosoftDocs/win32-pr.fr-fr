---
description: Spécifie une fenêtre pour le moteur multimédia qui applique des protections de sortie Protection Manager (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Attribut MF_MEDIA_ENGINE_OPM_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953377"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>Attribut de HWND de l’un des \_ Media \_ Engines \_ OPM \_

Spécifie une fenêtre pour le moteur multimédia qui applique des protections de [sortie Protection Manager](output-protection-manager.md) (OPM).

## <a name="data-type"></a>Type de données

**HWND** stocké comme **UINT64**

## <a name="remarks"></a>Notes

Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia.

Pour activer les protections OPM pour la lecture vidéo, l’application doit effectuer l’une des opérations suivantes :

-   Définissez l' [attribut \_ \_ HWND de \_ lecture \_ du moteur multimédia MF](mf-media-engine-playback-hwnd.md) lors de la création du moteur multimédia.
-   Définissez l' \_ attribut du \_ \_ HWND OPM Media Engine \_ pour la création du moteur multimédia.
-   Appelez [**IMFMediaEngineProtectedContent :: SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) à tout moment après avoir créé le moteur multimédia, mais avant d’afficher le contenu protégé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du moteur multimédia](media-engine-attributes.md)
</dt> </dl>

 

 





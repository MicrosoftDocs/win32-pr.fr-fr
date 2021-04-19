---
description: Une fois que votre extension de composant logiciel enfichable d’attachement s’est ajoutée au nœud services, elle doit établir la communication avec le composant logiciel enfichable Configuration de la sécurité.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Établissement de la communication avec les composants logiciels enfichables de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fe9bcb80687fa50120d20594a81ea40b21c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534648"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a>Établissement de la communication avec les composants logiciels enfichables de configuration

Une fois que votre extension de composant logiciel enfichable d’attachement s’est ajoutée au nœud services, elle doit établir la communication avec le composant logiciel enfichable Configuration de la sécurité. Cela est nécessaire, car l’extension du composant logiciel enfichable d’attachement obtient ses données, ainsi que toutes les modifications apportées par l’utilisateur, à partir du composant logiciel enfichable Configuration de la sécurité. Cela peut être effectué comme décrit dans la procédure suivante.

**Pour établir la communication avec les composants logiciels enfichables de configuration de la sécurité**

1.  Obtenez le nom du fichier de configuration à l’aide du \_ \_ format de presse-papiers CCF SCESVC joint, qui retourne le nom du fichier de configuration en tant que **PWSTR**.

    Si la pièce jointe est insérée sous un nœud de type de configuration, la pièce jointe doit connaître la configuration. (Il communique ces informations aux composants logiciels enfichables de configuration de sécurité lors de l’initialisation de l’interface.) Dans ce cas, utilisez le code suivant.

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  Configurez le contexte avec les composants logiciels enfichables de configuration de la sécurité. Une fois le nom de la configuration connu, ou si le nœud de service est un nœud d’analyse, l’extension du composant logiciel enfichable d’attachement doit appeler [**ISceSvcAttachmentData :: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) pour configurer le contexte, comme illustré dans l’exemple suivant.

    ```C++
    LPSCESVCATTACHMENTPERSISTINFO pSceInfo;

        HRESULT hr = ((LPSCESVCATTACHMENTPERSISTINFO)this)->
                QueryInterface(IID_ISceSvcAttachmentPersistInfo,
                (void**)&pSceInfo);

        if ( SUCCEEDED(hr) )
        {

            hr = m_pSceData->Initialize(strServiceName, TemplateName,
                    pSceInfo, &ThisHandle);
            // Continue processing (not shown).
        }
    ```

    

> [!Note]  
> Lorsque vous avez terminé d’utiliser le handle retourné par [**ISceSvcAttachmentData :: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), fermez le handle en appelant la fonction [**ISceSvcAttachmentData :: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) . Cette opération est généralement effectuée lorsque l’utilisateur ferme la console MMC.

 

 

 




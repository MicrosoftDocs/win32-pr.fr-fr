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
# <a name="establishing-communication-with-configuration-snap-ins"></a><span data-ttu-id="50199-103">Établissement de la communication avec les composants logiciels enfichables de configuration</span><span class="sxs-lookup"><span data-stu-id="50199-103">Establishing Communication with Configuration Snap-ins</span></span>

<span data-ttu-id="50199-104">Une fois que votre extension de composant logiciel enfichable d’attachement s’est ajoutée au nœud services, elle doit établir la communication avec le composant logiciel enfichable Configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="50199-104">After your attachment snap-in extension has added itself to the Services node, it should establish communication with the Security Configuration snap-in.</span></span> <span data-ttu-id="50199-105">Cela est nécessaire, car l’extension du composant logiciel enfichable d’attachement obtient ses données, ainsi que toutes les modifications apportées par l’utilisateur, à partir du composant logiciel enfichable Configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="50199-105">This is necessary because the attachment snap-in extension gets its data, as well as any changes made by the user, from the Security Configuration snap-in.</span></span> <span data-ttu-id="50199-106">Cela peut être effectué comme décrit dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="50199-106">This can be done as described in the following procedure.</span></span>

<span data-ttu-id="50199-107">**Pour établir la communication avec les composants logiciels enfichables de configuration de la sécurité**</span><span class="sxs-lookup"><span data-stu-id="50199-107">**To establish communication with the Security Configuration snap-ins**</span></span>

1.  <span data-ttu-id="50199-108">Obtenez le nom du fichier de configuration à l’aide du \_ \_ format de presse-papiers CCF SCESVC joint, qui retourne le nom du fichier de configuration en tant que **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="50199-108">Obtain the configuration file name using the CCF\_SCESVC\_ATTACHMENT clipboard format, which returns the configuration file name as a **PWSTR**.</span></span>

    <span data-ttu-id="50199-109">Si la pièce jointe est insérée sous un nœud de type de configuration, la pièce jointe doit connaître la configuration.</span><span class="sxs-lookup"><span data-stu-id="50199-109">If the attachment is inserted under a configuration type node, the attachment needs to know which configuration it is.</span></span> <span data-ttu-id="50199-110">(Il communique ces informations aux composants logiciels enfichables de configuration de sécurité lors de l’initialisation de l’interface.) Dans ce cas, utilisez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="50199-110">(It communicates this information to the Security Configuration snap-ins during interface initialization.) In this case, use the following code.</span></span>

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  <span data-ttu-id="50199-111">Configurez le contexte avec les composants logiciels enfichables de configuration de la sécurité. Une fois le nom de la configuration connu, ou si le nœud de service est un nœud d’analyse, l’extension du composant logiciel enfichable d’attachement doit appeler [**ISceSvcAttachmentData :: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) pour configurer le contexte, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="50199-111">Set up the context with the Security Configuration snap-ins. After the configuration name is known, or if the service node is an analysis node, the attachment snap-in extension must call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to set up the context, as shown in the following example.</span></span>

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
> <span data-ttu-id="50199-112">Lorsque vous avez terminé d’utiliser le handle retourné par [**ISceSvcAttachmentData :: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), fermez le handle en appelant la fonction [**ISceSvcAttachmentData :: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="50199-112">When you have finished using the handle returned by [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), close the handle by calling the [**ISceSvcAttachmentData::CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) function.</span></span> <span data-ttu-id="50199-113">Cette opération est généralement effectuée lorsque l’utilisateur ferme la console MMC.</span><span class="sxs-lookup"><span data-stu-id="50199-113">This is typically done when the user closes the MMC console.</span></span>

 

 

 




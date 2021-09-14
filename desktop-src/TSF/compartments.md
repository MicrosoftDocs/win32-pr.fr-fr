---
title: Compartiments
description: Compartiments
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Text Services Framework (TSF), compartiments
- TSF (Text Services Framework), compartiments
- services de texte, compartiments
- Applications compatibles TSF, compartiments
- compartiments
- Text Services Framework (TSF), types de compartiments
- TSF (Text Services Framework), types de compartiments
- services de texte, types de compartiments
- Applications compatibles TSF, types de compartiments
- types de compartiments
- Text Services Framework (TSF), notifications de modification de compartiment
- TSF (Text Services Framework), notifications de modification de compartiment
- services de texte, notifications de modification de compartiments
- Applications compatibles TSF, notifications de modification de compartiments
- notifications de modification de compartiment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193564"
---
# <a name="compartments"></a>Compartiments

## <a name="compartment-types"></a>Types de compartiments

Il existe différents types de compartiments. Il existe un compartiment global, et chaque gestionnaire de threads, le gestionnaire de documents et le contexte peuvent contenir un compartiment.

Le compartiment global permet aux clients de partager des données entre les processus. Pour obtenir le gestionnaire de compartiments globaux, appelez [**ITfThreadMgr :: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).

Le gestionnaire de thread contient un gestionnaire de compartiments qui contient des compartiments pour chaque thread. Cela permet de partager des données au sein d’un thread. Pour obtenir un gestionnaire de compartiments du gestionnaire de threads, appelez **ITfThreadMgr :: QueryInterface** avec IID \_ ITfCompartmentMgr.

Chaque gestionnaire de documents créé contient également un gestionnaire de compartiments. Cela permet de partager des données dans un gestionnaire de document spécifique. Pour obtenir le gestionnaire de compartiments du gestionnaire de documents, appelez **ITfDocumentMgr :: QueryInterface** avec IID \_ ITfCompartmentMgr.

Chaque contexte créé contient également un gestionnaire de compartiments. Cela permet de partager des données dans un contexte spécifique. Pour obtenir un gestionnaire de compartiments de contexte, appelez **ITfContext :: QueryInterface** avec IID \_ ITfCompartmentMgr.

## <a name="creating-and-deleting-a-compartment"></a>Création et suppression d’un compartiment

Un compartiment est créé la première fois que [**ITfCompartmentMgr :: GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) est appelé avec le GUID de compartiment. Le client d’installation doit définir la valeur initiale du compartiment à l’aide de [**ITfCompartment :: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue). Tant qu’une valeur n’est pas définie, la valeur de compartiment est vide. Pour cette raison, il n’existe aucun moyen de vérifier que le compartiment existait avant l’appel de **GetCompartment** . Pour éviter cette situation, le client d’installation doit définir la valeur sur une valeur initiale afin que d’autres clients puissent déterminer si le compartiment existe déjà.

La méthode [**ITfCompartmentMgr :: ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) est utilisée pour supprimer un compartiment. Toute référence existante au compartiment est marquée comme non valide.

## <a name="obtaining-compartments"></a>Obtention de compartiments

À l’aide de l’interface [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) , un client peut énumérer des compartiments en appelant [**ITfCompartmentMgr :: EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments). Cette méthode fournit un objet **IEnumGUID** qui contient les GUID de tous les compartiments installés.

À l’aide du GUID de compartiment, **ITfCompartmentMgr :: GetCompartment** est utilisé pour obtenir un compartiment spécifique. Cette méthode fournit à l’appelant un objet [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) qui peut obtenir et définir les données de compartiment.

## <a name="receiving-compartment-change-notifications"></a>Notifications de modification des compartiments de réception

Lorsque la valeur d’un compartiment change, le gestionnaire TSF avertit tous les récepteurs de notification installés que le compartiment a changé. Pour installer un récepteur de notification de changement de compartiment, créez un objet qui implémente [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink). Appelez ensuite **ITfCompartment :: QueryInterface** avec IID \_ ITfSource sur l’objet compartiment à surveiller pour obtenir une interface [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) . À présent, appelez [**ITfSource :: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) avec IID \_ ITfCompartmentEventSink et le pointeur vers l’objet **ITfCompartmentEventSink** . Lorsque la valeur du compartiment change, [**ITfCompartmentEventSink :: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) du récepteur de notifications est appelé avec le GUID du compartiment. Le récepteur de notifications peut appeler [**ITfCompartment :: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) pour obtenir la nouvelle valeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[**TfClientId**](tfclientid.md)
</dt> <dt>

[**ITfThreadMgr :: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[**ITfCompartment :: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**ITfSource :: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**ITfCompartmentEventSink :: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 





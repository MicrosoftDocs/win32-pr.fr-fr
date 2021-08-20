---
title: Gestion des erreurs COM dans Java et Visual Basic
description: Gestion des erreurs COM dans Java et Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba8e179ca3e7a1d57fdae63e8ad20d14a6fff358fab1fff24bfe7ae8df185d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048517"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>Gestion des erreurs COM dans Java et Visual Basic

Il existe trois interfaces et trois fonctions qui peuvent être utilisées dans COM pour assurer la gestion des erreurs lors de la programmation en Java ou Microsoft Visual Basic. en Java et Visual Basic, l’appel de méthode ne retourne pas de valeur **HRESULT** comme valeur de retour. Au lieu de cela, ces langages utilisent les interfaces et les fonctions COM pour obtenir des valeurs **HRESULT** et pour gérer les erreurs ou les exceptions. (Les exceptions sont des événements qui se trouvent au-delà du contrôle du programme, tels que des problèmes de fichier ou des paramètres non valides.)

Les trois interfaces qui assurent la prise en charge de **HRESULT** s sont répertoriées et décrites brièvement dans le tableau suivant.



|  Interface                                                                        |  Description                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Définit les informations d’erreur.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Retourne des informations à partir d’un objet d’erreur.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Identifie l’objet comme prenant en charge l’interface [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .<br/> |



 

Les trois fonctions qui assurent la prise en charge de **HRESULT** s sont répertoriées et décrites brièvement dans le tableau suivant.



|    Interface       |       Description       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Crée une instance d’un objet d’erreur générique.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Obtient le pointeur d’informations d’erreur défini par l’appel précédent à [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) dans le thread logique actuel.<br/> |
| [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Définit l’objet d’informations d’erreur pour le thread d’exécution actuel.<br/>                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM](error-handling-in-com.md)
</dt> </dl>

 


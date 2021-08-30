---
description: Supposons que le fournisseur de services doit afficher une boîte de dialogue (par exemple, la boîte de dialogue Unimodem ou ATSP) pendant le traitement de lineMakeCall ou lineDial.
ms.assetid: 46f87947-bfcd-48ad-8c33-7ea4d9caa34c
title: Fonctions non conçues pour générer l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a0cfb8168f4338ca5263abc067b141338caf1e24bef68c21241cfd6e53690d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013209"
---
# <a name="functions-not-designed-to-generate-ui"></a>Fonctions non conçues pour générer l’interface utilisateur

Supposons que le fournisseur de services doit afficher une boîte de dialogue (par exemple, **la boîte de** dialogue Unimodem ou ATSP) pendant le traitement de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) ou [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial). Dans ce cas, il s’agit du fournisseur de services, et non de l’application, qui décide que l’interface utilisateur doit être affichée.

Pour appeler la DLL de l’interface utilisateur dans le processus d’application, le fournisseur de services appelle le rappel d' [*\_ événement de ligne*](/windows/win32/api/tspi/nc-tspi-lineevent) TSPI, en générant un message de [**ligne \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) , en passant un pointeur vers une structure de type [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams). Cette structure contient le **dwRequestID** de la fonction à laquelle l’interface utilisateur est associée, ce qui permet à tapisrv d’identifier l’application cliente dans laquelle l’interface utilisateur doit être générée.

TAPISRV demande l’instance appropriée de l’interface TAPI pour charger la DLL de l’interface utilisateur et créer un thread pour l’interface utilisateur dans le processus de l’application. À partir de ce nouveau thread d’interface utilisateur, TAPI appelle la fonction [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) de la dll de l’interface utilisateur, en transmettant les données spécifiées par le fournisseur de services de téléphonie dans la structure passée avec le message de [**ligne \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) . la dll de l’interface utilisateur affiche la boîte de dialogue appropriée (qui est une question pour la conception privée entre la dll de l’interface utilisateur et le fournisseur La DLL de l’interface utilisateur n’est pas retournée à partir de **TUISPI \_ providerGenericDialog** jusqu’à la fermeture de la boîte de dialogue.

Le fournisseur de services de téléphonie peut générer des données mises à jour pour s’afficher dans la boîte de dialogue (ou, par exemple, pour indiquer que la boîte de dialogue doit être fermée, si l’appel est abandonné ou si d’autres événements se produisent) en envoyant un message de [**ligne \_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md) . TAPISRV transmet les données à l’interface TAPI, qui appelle la fonction [**\_ providerGenericDialogData TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) de la dll de l’interface utilisateur. Ce mécanisme fournit une « transmission » unidirectionnelle à la DLL de l’interface utilisateur. Si la DLL de l’interface utilisateur souhaite informer le fournisseur de services de téléphonie des résultats de la boîte de dialogue ou obtenir d’autres données, elle peut appeler la fonction [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) (pointeur vers lequel elle a été reçue lors de l’appel de [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) ).

Quand la boîte de dialogue est fermée, [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) retourne à l’interface TAPI. L’interface TAPI appelle [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) pour libérer la dll de l’interface utilisateur et quitte le thread d’interface utilisateur qu’elle avait créé dans le contexte de l’application. Il demande ensuite à TAPISRV d’appeler la fonction [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) du fournisseur de services de téléphonie pour dissocier l’association créée lorsque le fournisseur de services de téléphonie a envoyé à l’origine le message de [**ligne \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) . Cette fonction est également appelée si le processus d’application se termine de manière inattendue avant le retour de **TUISPI \_ providerGenericDialog** .

 

 

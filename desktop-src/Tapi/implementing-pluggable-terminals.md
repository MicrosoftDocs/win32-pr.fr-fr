---
description: Les exigences générales relatives à l’implémentation d’un terminal enfichable sont répertoriées ci-dessous.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implémentation de terminaux enfichables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 494b2f6bc5ccb214bc7101f570a4db3037fd8cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518729"
---
# <a name="implementing-pluggable-terminals"></a>Implémentation de terminaux enfichables

Les exigences générales en matière d’implémentation de terminal enfichable sont les suivantes :

-   Le code de diffusion en continu sous-jacent d’un terminal enfichable doit correspondre aux capacités des MSP souhaités.
-   Le terminal doit utiliser des filtres DirectShow pour travailler avec la plupart des MSP (cela est supposé ici sur).
-   Les terminaux audio doivent prendre en charge le PCM linéaire mono 16 bits 8 kHz pour la plupart des MSP.
-   Le terminal doit activer le marshaling de threads libres en implémentant [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). Pour ce faire, le terminal peut appeler l’API COM [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) et agréger **IMarshal** au pointeur retourné. Le destructeur de l’objet terminal doit appeler [**IMarshal->Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).
-   Le terminal doit implémenter ou agréger toutes les interfaces supplémentaires spécifiques au terminal qui sont appropriées.
-   L’implémentation du terminal doit être thread-safe.
-   L’implémentation de terminal doit \# inclure termmgr. h pour la définition de [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol). Cela s’ajoute aux fichiers include et libs habituels qui sont nécessaires pour les applications TAPI 3 ou TAPI 3 sous Windows 2000 SP1.

Remarques sur l’implémentation des interfaces et des méthodes :

Le terminal doit implémenter [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (interface double – vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)).

[**ITTerminal :: obtient \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

Le terminal doit retourner une représentation **BSTR** d’un GUID que vous avez choisi pour identifier votre type de terminal. Allouez le **BSTR** via [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Pour convertir un GUID en **BSTR**, appelez [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid), **SysAllocString** et [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

[**ITTerminal :: obtient \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

Le terminal doit généralement retourner TT \_ dynamique si une application implémente le terminal. Le retour de TT \_ static fonctionne également et le retour de cette valeur peut être approprié si le terminal correspond à un périphérique matériel. Toutefois, cette opération peut être déroutante pour les utilisateurs car un terminal statique ne sera pas présent dans l’énumération des terminaux statiques du MSP.

[**ITTerminal :: obtient l' \_ État**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Si l’implémentation de terminal ne limite pas arbitrairement le nombre de flux auxquels le terminal peut être connecté simultanément, le terminal doit toujours retourner TS \_ NOTINUSE.

Dans le cas contraire, l’implémentation de terminal limite arbitrairement le nombre de flux auxquels le terminal peut être connecté à la fois. Dans ce cas, le terminal doit conserver le nombre de flux auxquels il est connecté. Le terminal doit incrémenter ce nombre interne lors de la réussite de l’appel de [**ITTerminalControl :: ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) et le décrémenter sur un appel de [**ITTerminalControl ::D isconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) réussi. Dans [**ITTerminal :: obtenir l' \_ État**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state), elle doit retourner TS \_ Inuse si ce nombre est égal au nombre maximal de flux que le terminal peut sélectionner à la fois ; sinon, il doit retourner TS \_ NOTINUSE. Notez que si la limite est définie sur un, le nombre peut simplement être une valeur booléenne ou d' \_ état terminal.

[**ITTerminal :: obtient le \_ nom**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

Le terminal doit retourner un nom **BSTR** de son choix, alloué via [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring). Ce nom doit être significatif pour l’utilisateur et doit être localisé.

[**ITTerminal :: obtient le \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

Le terminal doit retourner son type de média, TAPIMEDIATYPE \_ audio ou TAPIMEDIATYPE \_ Video.

[**ITTerminal :: obtient la \_ direction**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

Le terminal renvoie la \_ valeur d’énumération de la direction du terminal indiquant la direction du terminal. Si le terminal est bidirectionnel (par exemple, un pont), il doit retourner TD \_ bidirectionnel.

Le terminal doit implémenter [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (vtable uniquement).

[**ITTerminalControl :: obtient \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Un terminal fourni par l’application doit toujours retourner la **valeur null** comme handle d’adresse. Cela indique au MSP que ce terminal n’a pas été créé sur un objet d’adresse MSP spécifique.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

Sur cet appel, le terminal ajoute ses filtres au graphique donné et s’y connecte, le cas échéant. Le terminal doit ensuite renvoyer le ou les codes confidentiels exposés par le terminal pour la direction du flux spécifiée.

Un terminal qui ne prend pas en charge la connexion simultanée à plusieurs flux définit une variable interne sur TS \_ Inuse en cas de réussite de l’exécution de cette méthode.

Le terminal peut utiliser le paramètre *dwTerminalDirection* à partir de cet appel pour déterminer la direction du flux auquel il est connecté. Cela est nécessaire pour les terminaux bidirectionnels.

> [!Note]  
> En général (dans les classes de base MSP et dans tous les MSP connus), le code de flux MSP échoue à la connexion si le terminal renvoie plusieurs codes confidentiels à partir d’un seul appel [**ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) . Cela est parfait, car un terminal qui retourne plus d’un code confidentiel pendant la connexion requiert que le MSP ait une connaissance particulière du terminal pour pouvoir utiliser efficacement les codes confidentiels supplémentaires.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

Le terminal doit simplement retourner S \_ OK. Le terminal peut également effectuer une initialisation après la connexion si nécessaire.

[**ITTerminalControl ::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

Le terminal doit effectuer tout ce qui est nécessaire pour déconnecter le terminal du reste du graphique. En général, cela implique de supprimer tous les filtres des terminaux du graphique et de définir l’état du terminal sur TS \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

Le terminal doit simplement retourner E \_ NOTIMPL.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

Le terminal doit simplement retourner E \_ NOTIMPL.

 

 

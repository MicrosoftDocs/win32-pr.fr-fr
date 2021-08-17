---
title: Interface utilisateur de configuration de Client-Side
description: Le fournisseur qui implémente le protocole d’authentification peut également fournir une interface utilisateur de configuration pour le protocole.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c8b067ba65312edea412ba532620e029912088e9cc61885626f8a13f5a2834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117802"
---
# <a name="client-side-configuration-user-interface"></a>Interface utilisateur de configuration de Client-Side

Le fournisseur qui implémente le protocole d’authentification peut également fournir une interface utilisateur de configuration pour le protocole. L’interface utilisateur de configuration peut être implémentée dans la même DLL que le protocole d’authentification ou dans une DLL distincte. En outre, la DLL qui implémente l’interface utilisateur de configuration peut prendre en charge plusieurs protocoles d’authentification. Le chemin d’accès à la DLL de l’interface utilisateur de configuration est stocké dans la \_ \_ valeur de Registre RAS configui valueName \_ , sous la clé du protocole d’authentification. Pour plus d’informations sur la création de cette valeur de Registre, consultez la page [installation d’EAP](eap-installation.md).

La DLL de l’interface utilisateur de configuration doit exporter des points d’entrée pour les fonctions suivantes :

[**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Lorsque l’utilisateur crée une entrée de configuration pour une connexion particulière, que ce soit pour un client RAS ou sans fil, il peut sélectionner le protocole d’authentification que le service doit utiliser avec cette entrée. Si le protocole d’authentification est configurable, le service appelle [**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) pour appeler l’interface utilisateur de configuration. L’interface utilisateur de configuration stocke les informations de configuration retournées par **RasEapInvokeConfigUI** dans l’entrée de configuration.

Les informations de configuration doivent être génériques pour tous les utilisateurs de l’ordinateur client. Les informations spécifiques à un utilisateur ou à des utilisateurs particuliers ne doivent pas être stockées dans l’entrée. Le protocole d’authentification doit obtenir des informations spécifiques à l’utilisateur à l’aide des [fonctions d’identité](obtaining-identity-information.md) ou [de l’interface utilisateur interactive](interactive-user-interface.md). Le protocole d’authentification peut stocker ces informations dans le registre en les passant au service d’authentification dans le paramètre *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Les informations de configuration ne doivent pas non plus être spécifiques à l’ordinateur actuel. il doit être portable d’un ordinateur à l’ordinateur.

Lorsque le service d’authentification appelle la fonction [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) pour le protocole d’authentification, il passe une structure [**\_ \_ d’entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) qui contient un pointeur vers les informations de configuration. Une fois l’appel à **RasEapBegin** terminé, le service d’authentification appelle [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) pour libérer la mémoire occupée par les informations de configuration. Par conséquent, le protocole d’authentification doit copier les informations de configuration dans une mémoire tampon de mémoire privée pendant l’appel à **RasEapBegin**.

Le fournisseur peut ajouter une valeur sous la clé de Registre pour le protocole d’authentification qui spécifie les informations de configuration par défaut pour le protocole. Le fournisseur peut également ajouter une valeur qui spécifie si l’utilisateur doit entrer les informations de configuration lorsqu’il crée une entrée d’annuaire téléphonique. Pour plus d’informations, consultez [valeurs de Registre du protocole d’authentification](authentication-protocol-registry-values.md).

 

 
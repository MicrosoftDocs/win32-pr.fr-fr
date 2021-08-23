---
title: Obtention des informations d’identité
description: Le fournisseur qui implémente le protocole d’authentification peut également fournir une interface de fonction qui obtient des informations d’identification initiales pour l’utilisateur demandant l’authentification.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46245b22a5538fc347ba735620270b7bbc1071574852305adc6b3881202ae317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605819"
---
# <a name="obtaining-identity-information"></a>Obtention des informations d’identité

Le fournisseur qui implémente le protocole d’authentification peut également fournir une interface de fonction qui obtient des informations d’identification initiales pour l’utilisateur demandant l’authentification.

Le fournisseur doit implémenter les fonctions suivantes.

-   [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Ces fonctions peuvent être implémentées dans la même DLL que le protocole d’authentification ou dans une DLL distincte. En outre, la DLL qui implémente les fonctions d’identité peut prendre en charge plusieurs protocoles d’authentification. Le chemin d’accès à la DLL pour ces fonctions est stocké dans la valeur du registre de l' [ \_ \_ \_ identité du valueName EAP RAS](authentication-protocol-registry-values.md) , sous la clé du protocole d’authentification. Pour plus d’informations sur la création de cette valeur de Registre, consultez la page [installation d’EAP](eap-installation.md).

La fonction [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) affiche généralement une interface utilisateur (IU) pour obtenir les informations d’identité de l’utilisateur. Toutefois, si le paramètre *dwFlags* contient l’indicateur \_ non interactif de l’indicateur EAP RAS \_ \_ \_ , **RasEapGetIdentity** ne doit pas afficher d’interface utilisateur.

Si [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) affiche une interface utilisateur, l’interface utilisateur doit prendre en charge les messages de [**\_ commande WM**](../menurc/wm-command.md) où la valeur de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) est égale à IDCANCEL.

Le service d’authentification appelle [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) si la valeur NAMEDLG de l' [ \_ \_ \_ appel \_ du valueName EAP RAS](authentication-protocol-registry-values.md) qui se trouve dans le registre pour cet EAP est définie sur zéro. Si \_ \_ le nom d’appel d’accès distant EAP \_ \_ NAMEDLG n’est pas présent, s’il est présent et qu’il est défini sur un, le service d’authentification affiche la boîte de dialogue nom d’utilisateur système standard.

En plus de l’appel de NAMEDLG d’appel d’accès distant \_ EAP \_ \_ \_ , le fournisseur EAP peut créer une valeur associée, [RAS \_ EAP \_ valueName \_ Invoke \_ PWDDLG](authentication-protocol-registry-values.md), dans le registre. Si cette valeur est présente et définie à zéro, le service n’affiche pas la boîte de dialogue de mot de passe système standard. Cette valeur est utile lors de l’implémentation d’une méthode biométrique telle qu’une analyse d’empreintes digitales pour authentifier l’utilisateur. Si les valeurs PWDDLG des appels NAMEDLG et RAS du valueName EAP de l’appel d’accès distant EAP \_ \_ \_ \_ \_ \_ \_ \_ sont égales à zéro, une interface utilisateur d’identité peut être utilisée pour obtenir à la fois l’identité et les informations biométriques. Toutefois, si seul \_ l’appel de l’appel de méthode d’accès distant EAP \_ \_ \_ PWDDLG est égal à zéro, le service d’authentification n’appellera pas [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Dans ce cas, vous pouvez utiliser l' [interface utilisateur interactive](interactive-user-interface.md) pour obtenir les informations biométriques.

Pour plus d’informations sur ces valeurs de Registre, consultez [valeurs de Registre du protocole d’authentification](authentication-protocol-registry-values.md).

Les informations obtenues par [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) sont transmises au protocole d’authentification lors de l’appel à [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Les informations sont référencées par les membres **pszIdentity** et **pUserData** de la [**structure \_ \_ d’entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Pour enregistrer ces informations dans le registre sur l’ordinateur client, le protocole d’authentification doit renvoyer les informations dans le paramètre *pEapOutput* de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Après l’appel à [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), le service d’authentification appelle [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) pour libérer la mémoire occupée par ces données. Par conséquent, le protocole d’authentification doit copier les informations dans une mémoire tampon de mémoire privée pendant l’appel à **RasEapBegin**.

 

 
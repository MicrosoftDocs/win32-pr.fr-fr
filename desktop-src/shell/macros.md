---
description: cette section décrit les macros de l’utilitaire Windows Shell.
title: Macros de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0b43e4fb60f8cd1d486bd6c6eaab7dee657449331025c24a322803ca086b0ee1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049238"
---
# <a name="shell-macros"></a>Macros de Shell

cette section décrit les macros de l’utilitaire Windows Shell.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                  | Description                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DÉFINIR \_ PROPERTYKEY**](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | Utilisé pour empaqueter un identificateur de format (FMTID) et un identificateur de propriété (PID) dans une structure [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) qui représente une clé de propriété.<br/>                                                                                    |
| [**IID \_ PPV \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | Utilisé pour récupérer un pointeur d’interface, en fournissant automatiquement la valeur IID de l’interface demandée en fonction du type du pointeur d’interface utilisé. Cela évite une erreur de codage commune en vérifiant le type de la valeur passée au moment de la compilation.<br/> |
| [**IsEqualPropertyKey**](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | Compare les membres de deux structures [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) et retourne si elles sont égales.<br/>                                                                                                                                 |
| [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | Utilisé pour compresser les informations de version de DLL dans une valeur ULONGLONG.<br/>                                                                                                                                                                                         |
| [**DisplayErrorTip NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | Affiche un message d’erreur dans l’info-bulle associée au contrôle d’adresse réseau.<br/>                                                                                                                                                            |
| [**GetAddress NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | Indique si une adresse réseau est conforme à un type et un format spécifiés.<br/>                                                                                                                                                                         |
| [**GetAllowType NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | Récupère les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.<br/>                                                                                                                                                                |
| [**SetAllowType NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | Définit les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.<br/>                                                                                                                                                                     |



 

 

 

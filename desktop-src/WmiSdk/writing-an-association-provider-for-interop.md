---
description: Un fournisseur d’associations fournit un mécanisme permettant d’inscrire des profils et de les associer à des profils qui sont implémentés dans différents espaces de noms.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Écriture d’un fournisseur d’association pour l’interopérabilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106528585"
---
# <a name="writing-an-association-provider-for-interop"></a>Écriture d’un fournisseur d’association pour l’interopérabilité

Un fournisseur d’associations fournit un mécanisme permettant d’inscrire des profils et de les associer à des profils qui sont implémentés dans différents espaces de noms.

Les fournisseurs d’associations sont utilisés pour exposer des profils standard, comme un profil d’alimentation. Pour ce faire, vous devez écrire un fournisseur d’association dans l’espace de noms racine/Interop qui expose des instances d’association en implémentant une classe dérivée de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)). Le fournisseur doit être inscrit à la fois dans la racine/l’interopérabilité et dans la racine/l' <implemented> espace de noms pour prendre en charge la traversée d’espaces de noms croisés.

Windows Management Instrumentation (WMI) charge le fournisseur d’associations chaque fois qu’une requête d’association est exécutée dans l’espace de noms racine/Interop.

**Pour implémenter un fournisseur d’association pour l’interopérabilité**

1.  Dérivez une classe de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) et créez une instance statique de cette classe dérivée dans l' \\ espace de noms Interop racine. Au minimum, les propriétés suivantes doivent être propagées avec des valeurs valides :

    -   [**InstanceID**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredName**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Même si [**InstanceID**](/previous-versions//ee309375(v=vs.85)) définit de manière unique l’instance de **l' \_ RegisteredProfile CIM**, la combinaison de **RegisteredName**, **RegisteredOrganization** et **RegisteredVersion** doit identifier de façon unique le profil inscrit dans l’étendue de l’organisation. Pour plus d’informations sur les propriétés individuelles, voir [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

    L’exemple de code suivant décrit la syntaxe pour la dérivation de la classe **ProcessProfile** à partir de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) et le remplissage de l’instance statique.

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > Pour les clients Windows, la propriété **RegisteredOrganization** doit avoir la valeur 1 et la propriété **OtherRegisteredOrganization** définie sur « Microsoft ».

     

2.  Créez un fournisseur qui retourne les instances d’association des [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile). Il s’agit d’un processus en deux étapes.

    1.  Créez une classe dérivée de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) dans les espaces de noms Interop et implementation. Étant donné que le même profil peut être implémenté par des fournisseurs différents, le nom de la classe doit être unique. La Convention d’affectation de noms recommandée est « <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ». La propriété **ConformantStandard** ou **propriété ManagedElement** doit spécifier le qualificateur **\_ targetNamespace de msft** contenant l’espace de noms auquel appartient cette classe.

        L’exemple de code suivant décrit la syntaxe permettant de dériver \_ la \_ classe Microsoft process ElementConformsToProfile \_ v1 de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) dans l' \\ espace de noms Interop racine. Dans cet exemple, l' \_ élément géré par le processus Win32 fait référence à l' \\ espace de noms CIMV2 racine à l’aide du qualificateur **\_ targetNamespace de msft** .

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        L’exemple de code suivant décrit la syntaxe permettant de dériver \_ la \_ classe Microsoft process ElementConformsToProfile \_ v1 de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) dans l' \\ espace de noms CIMV2 racine. Dans cet exemple, la norme [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conforme fait référence à l' \\ espace de noms Interop racine à l’aide du qualificateur **\_ targetNamespace de msft** .

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Si le **qualificateur \_ targetNamespace de msft** n’est pas spécifié sur la propriété qui fait référence à l’espace de noms implémenté, le filtre **ResultClass** de l’instruction « associateurs de » ne fonctionnera pas. Par exemple, si le **qualificateur \_ targetNamespace msft** n’est pas spécifié, la ligne de commande Windows PowerShell suivante ne retourne pas d’objet : **obtenir-WmiObject-query "ASSOCIATORS of {ProcessProfile. InstanceId = 'Process'} WHERE ResultClass = 'Win32 \_ Process'**.

        Le **qualificateur \_ targetNamespace de msft** ne peut pas pointer vers un espace de noms sur un ordinateur distant. Par exemple, l’espace de noms suivant n’est pas pris en charge : msft \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ Interop racine).

    2.  Écrivez un fournisseur qui retourne des instances de la classe dérivée créée. Pour plus d’informations, consultez [écriture d’un fournisseur d’instances](writing-an-instance-provider.md). Lorsque vous accédez à des instances de plusieurs espaces de noms, vous devrez peut-être accéder aux niveaux de sécurité du client. Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).

        Le fournisseur d’associations doit implémenter à la fois les méthodes [**IWbemServices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) et [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) . L’implémentation de la méthode [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) est facultative. Étant donné que ce fournisseur est accessible à la fois à partir de l' \\ interopérabilité racine et des \\ <implemented> espaces de noms racine, il ne doit pas exister de dépendance explicite sur un espace de noms à l’intérieur du fournisseur.

3.  Inscrivez le fournisseur d’associations à la fois dans l' \\ interopérabilité racine et dans les \\ <implemented> espaces de noms racines. Pour plus d’informations, consultez [inscription d’un fournisseur d’instances](registering-an-instance-provider.md).

    L’exemple de code suivant décrit la syntaxe permettant d’inscrire le fournisseur d’associations dans l' \\ espace de noms Interop racine.

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    L’exemple de code suivant décrit la syntaxe permettant d’inscrire le fournisseur d’associations dans l' \\ espace de noms CIMV2 racine.

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  Placez le schéma pour le [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) dans l’espace de noms implémenté. Pour les clients Windows, il s’agit du fichier Interop. MOF qui se trouve dans le dossier% SystemRoot% \\ system32 \\ WBEM.
5.  Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.

    WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur. La méthode [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) doit être implémentée d’une manière qui lui permet d’être appelée pour deux espaces de noms différents. Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Écriture d’un fournisseur d’instances](writing-an-instance-provider.md)
</dt> <dt>

[Inscription d’un fournisseur d’instances](registering-an-instance-provider.md)
</dt> </dl>

 

 

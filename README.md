# apostila

Apostila React 
Nome do componente:NavigationContainer
Descrição do componente: o componemtem NavigatorContainer serve para criar uma tela inicial e uma tela de perfil para o seu 
sistema.
Exemplo de uso:

	<NavigationContainer>
            <AppStack.Navigator screenOptions={{headerShown: false}}>
                <AppStack.Screen name="Home" component={Home} />
                <AppStack.Screen name="Response" component={Response} />
            </AppStack.Navigator>
        </NavigationContainer>

link para o github do projeto: https://github.com/elioterio2002/IBGEsenai

link para video do yt: https://www.youtube.com/watch?v=cS4PgI3zBzY


Nome do componente:createStackNavigator
Descrição do componente: já o StackNavigator permite que o usuario possa interagir com o sistema.
Exemplo de uso:

	const AppStack = createStackNavigator();

import Home from './pages/index';
import Response from './pages/response';

export default function Routes(){
    return(
        <NavigationContainer>
            <AppStack.Navigator screenOptions={{headerShown: false}}>
                <AppStack.Screen name="Home" component={Home} />
                <AppStack.Screen name="Response" component={Response} />
            </AppStack.Navigator>
        </NavigationContainer>
    );
}

link para o github do projeto: https://github.com/elioterio2002/IBGEsenai

link para video do yt: https://www.youtube.com/watch?v=myhKI0B7eLw


Nome do componente:axios
Descrição do componente: o axios serve como mediador entre uma api externa e o react native.
Exemplo de uso:

	const api = axios.create({
   	 baseURL: 'https://servicodados.ibge.gov.br/api/v2/censos'
	});

	export default api;

link para o github do projeto: https://github.com/elioterio2002/IBGEsenai

link para video do yt: https://www.youtube.com/watch?v=fBrOtR3pgPU

Nome do componente:{View, Text, Image,KeyboardAvoidingView, TextInput, TouchableOpacity}
Descrição do componente: todos esses componentes pertencem ao front so sistema View(tela), Texto(texto do app), touchableo
pacity(botao).
Exemplo de uso:

	const [name,setName] = useState('');
    const [year,setYear] = useState(0);
    return(
        <KeyboardAvoidingView style={Styles.container}>
            <View style={Styles.header}>
                <Image source={Logo} />
            </View>
            <View style={Styles.body}>             
                <Text style={Styles.title}>Aplicativo de Nomes do IBGE</Text> 
                <TextInput placeholder='Digite seu nome (Apenas um nome)' onChangeText={(name) => {setName(name);}} placeholderTextColor='#000' style={Styles.input} />
                <TextInput keyboardType='numeric' placeholder='Ano de nascimento' onChangeText={(year) => {setYear(year);}} placeholderTextColor='#000' style={Styles.input} />
                <TouchableOpacity style={Styles.button} onPress={() => {IbgeController(name, year, navigation);}} ><Text style={Styles.buttonText}>Enviar</Text></TouchableOpacity>
            </View>
        </KeyboardAvoidingView>
    );
link para o github do projeto: https://github.com/elioterio2002/IBGEsenai

link para video do yt: https://www.youtube.com/watch?v=Xpg2x1ZZ9co

Nome do componente:StyleSheet
Descrição do componente: é uma versão mais robusta e completa do Css, basicamente o Css do React native, serve para estili
zar o app.
Exemplo de uso:

	cexport default StyleSheet.create({
    container: {
        flex:1,
        paddingHorizontal: 24,
        paddingTop: Constants.statusBarHeight+20
    },
link para o github do projeto: https://github.com/elioterio2002/IBGEsenai

link para video do yt: https://www.youtube.com/watch?v=lSTg5MFYSUA

Nome do componente:constant
Descrição do componente: serve para criar as animações do site, é um complemento do styleSheet
Exemplo de uso:

	cexport default StyleSheet.create({
    container: {
        flex:1,
        paddingHorizontal: 24,
        paddingTop: Constants.statusBarHeight+20
    },
link para o github do projeto: https://github.com/elioterio2002/IBGEsenai

link para video do yt: https://www.youtube.com/watch?v=lSTg5MFYSUA

Nome do componente:styled
Descrição do componente: responsavel pela "beleza" do app 
Exemplo de uso:

	cexport default StyleSheet.create({
    container: {
        flex:1,
        paddingHorizontal: 24,
        paddingTop: Constants.statusBarHeight+20
    },
link para o github do projeto: https://github.com/elioterio2002/IBGEsenai

link para video do yt: https://www.youtube.com/watch?v=OqpYDyY2kik

Nome do componente:useState
Descrição do componente: é o componente que permite conectar-se aos recursos do react. Extremamente importante
Exemplo de uso:

	import React, {useState} from 'react';
link para o github do projeto: https://github.com/elioterio2002/IBGEsenai

link para video do yt: https://www.youtube.com/watch?v=PFGjeNwUxR8


Nome do componente:asyncStorage
Descrição do componente: serve para guardar informações, de forma NÃO SEGURA.
Exemplo de uso:

	export default async function IbgeController(name, year, navigation){
    const response = await api.get('/nomes/' + name);
    const getName = response.data[0].nome;


link para o github do projeto: https://github.com/elioterio2002/IBGEsenai
link para video do yt: https://www.youtube.com/watch?v=4RcGoAoL9WY





